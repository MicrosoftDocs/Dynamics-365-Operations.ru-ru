---
title: "Правила элиминирования"
description: "Этот раздел содержит сведения о правилах исключения и различных вариантах для отчетности об исключениях."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 818572a8d1f790aaa7c6e4befc1d2222a1c35c50
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="elimination-rules"></a><span data-ttu-id="765af-103">Правила элиминирования</span><span class="sxs-lookup"><span data-stu-id="765af-103">Elimination rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="765af-104">Этот раздел содержит сведения о правилах исключения и различных вариантах для отчетности об исключениях.</span><span class="sxs-lookup"><span data-stu-id="765af-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="765af-105">Проводки исключений требуются, когда головная компания осуществляет коммерческую деятельность с одной или несколькими дочерними компаниями и использует консолидированную финансовую отчетность.</span><span class="sxs-lookup"><span data-stu-id="765af-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="765af-106">Консолидированные финансовые отчеты должны включать только проводки, которые происходят между консолидированной организацией и другими организациями за ее пределами.</span><span class="sxs-lookup"><span data-stu-id="765af-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="765af-107">Поэтому проводки между компаниями, находящимися в одной организации, должны быть удалены или исключены из ГК, чтобы они не появлялись в финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="765af-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="765af-108">Несколько способов сообщения о закрытиях:</span><span class="sxs-lookup"><span data-stu-id="765af-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="765af-109">Правило элиминирования можно создать и обработать в компании консолидации или элиминирования.</span><span class="sxs-lookup"><span data-stu-id="765af-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="765af-110">Финансовую отчетность можно использовать для того, чтобы показать закрытия, счета и аналитики в конкретной строке или столбце.</span><span class="sxs-lookup"><span data-stu-id="765af-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="765af-111">Отдельно юридическое лицо можно использовать для разноски ручных записей проводок, чтобы отслеживать закрытия.</span><span class="sxs-lookup"><span data-stu-id="765af-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="765af-112">Эта тема описывает правила элиминирования, которые обрабатываются в компании консолидации или элиминирования.</span><span class="sxs-lookup"><span data-stu-id="765af-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="765af-113">Можно настроить правила исключения, чтобы создать проводки исключения в компании, указанной как компания-получатель для исключений.</span><span class="sxs-lookup"><span data-stu-id="765af-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="765af-114">Эта компания-получатель называется компанией для исключения.</span><span class="sxs-lookup"><span data-stu-id="765af-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="765af-115">Имеется возможность создать журналы исключения в ходе процесса консолидации или с помощью предложения журнала исключений.</span><span class="sxs-lookup"><span data-stu-id="765af-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="765af-116">Прежде чем настраивать правила исключения, следует ознакомиться со следующими терминами:</span><span class="sxs-lookup"><span data-stu-id="765af-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="765af-117">**Исходное юридическое лицо** — юридическое лицо, в котором были разнесены суммы, которые будут закрываться.</span><span class="sxs-lookup"><span data-stu-id="765af-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="765af-118">**Конечное юридическое лицо** — юридическое лицо, в котором разнесены правила элиминирования.</span><span class="sxs-lookup"><span data-stu-id="765af-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="765af-119">**Юридическое лицо элиминирования** — юридическое лицо, указанное как конечное юридическое лицо для закрытия.</span><span class="sxs-lookup"><span data-stu-id="765af-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="765af-120">**Консолидированное юридическое лицо** — юридическое лицо, созданное для отчета о финансовых результатах для группы юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="765af-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="765af-121">Финансовые данные из компании консолидируются в эту компанию, а затем создается финансовый отчет с использованием объединенных данных.</span><span class="sxs-lookup"><span data-stu-id="765af-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="765af-122">Ниже приведена таблица с проводками, которые возможно будет необходимо исключить.</span><span class="sxs-lookup"><span data-stu-id="765af-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="765af-123">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="765af-123">Transaction type</span></span></th>
<th><span data-ttu-id="765af-124">пример</span><span class="sxs-lookup"><span data-stu-id="765af-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="765af-125">Ввод заказа на продажу и выставление накладной (централизованная обработка)</span><span class="sxs-lookup"><span data-stu-id="765af-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="765af-126">Продажа продукта клиенту от имени другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-127">Ввод заказа на продажу (внутрихолдинговый/внутрифирменный) и выставление накладной</span><span class="sxs-lookup"><span data-stu-id="765af-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="765af-128">Продажа продуктов между компаниями в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="765af-129">Заказы на покупку (централизованная обработка)</span><span class="sxs-lookup"><span data-stu-id="765af-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="765af-130">Приобретение запасов, расходных материалов, услуг, основных средств и других продуктов у поставщика от имени другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-131">Управление запасами (внутрихолдинговое/внутрифирменное)</span><span class="sxs-lookup"><span data-stu-id="765af-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="765af-132">Перемещение запасов одной компании в основные средства другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="765af-133">Перемещение запасов одной компании в запасы другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="765af-134">Отслеживание запасов в пути</span><span class="sxs-lookup"><span data-stu-id="765af-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="765af-135">Номенклатура перемещается между складами одной и той же компании, но размещенными на разных узлах.</span><span class="sxs-lookup"><span data-stu-id="765af-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-136">Централизованная обработка накладных для расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="765af-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="765af-137">Накладная выписывается на другую компанию в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="765af-138">Централизованная обработка платежей для расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="765af-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="765af-139">Накладная оплачивается от имени другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-140">Управление денежными средствами и казначейство (централизованная обработка)</span><span class="sxs-lookup"><span data-stu-id="765af-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="765af-141">Обрабатываются налоговые платежи, возвраты налогов, выплаты процентов, ссуд, авансовых платежей, выплаты по дивидендам и предоплаченные авторские отчисления или комиссионные.</span><span class="sxs-lookup"><span data-stu-id="765af-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="765af-142">Расходы оплачиваются от имени другой компании в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="765af-143">Накладная вводится в журналы компании-получателя и пользователь должен выполнить настройки между компаниями.</span><span class="sxs-lookup"><span data-stu-id="765af-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="765af-144">Например, одна компания оплачивает отчет по расходам сотрудника другой компании.</span><span class="sxs-lookup"><span data-stu-id="765af-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="765af-145">В этом случае в отчете по расходам сотрудника содержатся расходы, связанные с другой компанией.</span><span class="sxs-lookup"><span data-stu-id="765af-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="765af-146">Наличные деньги переводятся от одной компании к другой в своей организации.</span><span class="sxs-lookup"><span data-stu-id="765af-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="765af-147">Расчеты с клиентами (централизованная обработка)</span><span class="sxs-lookup"><span data-stu-id="765af-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="765af-148">Получение наличных денег для накладной клиента другой компании и депонирование чека на банковский счет компании.</span><span class="sxs-lookup"><span data-stu-id="765af-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-149">Зарплата (централизованная обработка, внутрихолдинговая/внутрифирменная)</span><span class="sxs-lookup"><span data-stu-id="765af-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="765af-150">Выплата зарплаты другой компании.</span><span class="sxs-lookup"><span data-stu-id="765af-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="765af-151">Например, компания оплачивает зарплату своим сотрудникам, но возвращает оплату работы, выполненной сотрудником для другой компании в течение этого периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="765af-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="765af-152">Или, если сотрудник работал половину времени на компанию А и половину — на компанию В, и льготы распространяются на все выплаты, это относится к обеим компаниям.</span><span class="sxs-lookup"><span data-stu-id="765af-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="765af-153">В этих случаях зарплата сотрудника включает в себя оплату от обеих компаний.</span><span class="sxs-lookup"><span data-stu-id="765af-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="765af-154">Разносятся не только зарплаты, но также и налоги, льготы, удержания и начисления на зарплату.</span><span class="sxs-lookup"><span data-stu-id="765af-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="765af-155">Перенос затрат труда из одного отдела или отделения в другой.</span><span class="sxs-lookup"><span data-stu-id="765af-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="765af-156">Основные средства (внутрихолдинговые/внутрифирменные)</span><span class="sxs-lookup"><span data-stu-id="765af-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="765af-157">Перемещение основных средств в основные средства или запасы другой компании.</span><span class="sxs-lookup"><span data-stu-id="765af-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="765af-158">Распределения (внутрихолдинговые/внутрифирменные)</span><span class="sxs-lookup"><span data-stu-id="765af-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="765af-159">Запускается процесс распределения.</span><span class="sxs-lookup"><span data-stu-id="765af-159">You process corporate allocations.</span></span> <span data-ttu-id="765af-160">Распределениями являются действия на любой счет, который выделен, независимо от исходного модуля.</span><span class="sxs-lookup"><span data-stu-id="765af-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="765af-161">пример</span><span class="sxs-lookup"><span data-stu-id="765af-161">Example</span></span>
<span data-ttu-id="765af-162">Ваша компания, компания А, продает устройства другой компании в вашей организации, компании В. В следующем примере показывается, каким образом проводки, возникающие между двумя компаниями, могут быть исключены.</span><span class="sxs-lookup"><span data-stu-id="765af-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="765af-163">Компания А продает компании В устройство, которое стоит 10,00, за 10,00.</span><span class="sxs-lookup"><span data-stu-id="765af-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="765af-164">Компания А продает компании В устройство, которое стоит 10,00, за 10,00 и берет 2,00 в стоимость доставки.</span><span class="sxs-lookup"><span data-stu-id="765af-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="765af-165">Компания А продает компании В устройство, которое стоит 10,00, за 15,00 и признает маржу от продажи.</span><span class="sxs-lookup"><span data-stu-id="765af-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="765af-166">Юридическое лицо А продает юридическому лицу В устройство, которое стоит 10,00, за 15,00 и признает половину маржи от продажи.</span><span class="sxs-lookup"><span data-stu-id="765af-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="765af-167">Компания В признает вторую половину маржи от продажи.</span><span class="sxs-lookup"><span data-stu-id="765af-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="765af-168">Поэтому, выручка разделена.</span><span class="sxs-lookup"><span data-stu-id="765af-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="765af-169">Разделенная выручка побуждает компанию делать заказы в другой компании внутри организации, а не в сторонней организации.</span><span class="sxs-lookup"><span data-stu-id="765af-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="765af-170">В результате этих проводок создаются внутрихолдинговые проводки, которые разносятся на кредитуемый и дебетуемый счета.</span><span class="sxs-lookup"><span data-stu-id="765af-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="765af-171">Кроме того, эти проводки могут включать суммы наценки и снижения цены, если сумма внутрихолдинговых продаж и стоимость проданных товаров не равны.</span><span class="sxs-lookup"><span data-stu-id="765af-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="765af-172">Настройка правил исключения</span><span class="sxs-lookup"><span data-stu-id="765af-172">Set up elimination rules</span></span>
<span data-ttu-id="765af-173">При настройке правил исключения в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition рекомендуется создать финансовую аналитику специально для целей исключения.</span><span class="sxs-lookup"><span data-stu-id="765af-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="765af-174">Большинство клиентов называют ее "Торговый партнер" или аналогично.</span><span class="sxs-lookup"><span data-stu-id="765af-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="765af-175">Если вы решите не использовать финансовую аналитику, необходимо обязательно иметь счета ГК, относящиеся только к внутрихолдинговым проводкам.</span><span class="sxs-lookup"><span data-stu-id="765af-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="765af-176">Настройка для исключений находится в области "Настройка" модуля "Консолидации".</span><span class="sxs-lookup"><span data-stu-id="765af-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="765af-177">После ввода описания для правила необходимо выбрать компанию, в которую будет выполняться разноска журнала исключений.</span><span class="sxs-lookup"><span data-stu-id="765af-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="765af-178">Это должна быть компания, для которой в настройке юридического лица выбрано **Использовать для процесса финансового закрытия**.</span><span class="sxs-lookup"><span data-stu-id="765af-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="765af-179">Можно задать дату вступления в силу правила исключения и дату истечения срока его действия, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="765af-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="765af-180">Необходимо установить для параметра **Активное** значение **Да**, если необходимо, чтобы оно было доступно в процессе предложения элиминирования.</span><span class="sxs-lookup"><span data-stu-id="765af-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="765af-181">Выберите имя журнала, который имеет тип **Элиминирование**.</span><span class="sxs-lookup"><span data-stu-id="765af-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="765af-182">После определения основных параметров, можно задать фактические правила обработки, щелкнув **Строки**.</span><span class="sxs-lookup"><span data-stu-id="765af-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="765af-183">Существует два варианта для исключений: исключение суммы чистого изменения или определение фиксированной суммы.</span><span class="sxs-lookup"><span data-stu-id="765af-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="765af-184">Выберите свой исходный счет.</span><span class="sxs-lookup"><span data-stu-id="765af-184">Select your source account.</span></span> <span data-ttu-id="765af-185">Можно использовать звездочку (\*) как подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="765af-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="765af-186">Например, 1\* выбирает все счета, начинающиеся на 1, как исходные данные для распределения.</span><span class="sxs-lookup"><span data-stu-id="765af-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="765af-187">После выбора исходных счетов поле **Спецификация счета** определяет счет из компании-получателя, который используется.</span><span class="sxs-lookup"><span data-stu-id="765af-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="765af-188">Выберите **Источник**, если необходимо использовать тот же счет ГК, что и определенный в счете **Источник**.</span><span class="sxs-lookup"><span data-stu-id="765af-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="765af-189">При выборе варианта **Определенный пользователем**, необходимо указать счет назначения.</span><span class="sxs-lookup"><span data-stu-id="765af-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="765af-190">Указание аналитики действует таким же образом.</span><span class="sxs-lookup"><span data-stu-id="765af-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="765af-191">При выборе **Источник** будут использоваться те же аналитики в компании-получателе, что и в компании-источнике.</span><span class="sxs-lookup"><span data-stu-id="765af-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="765af-192">При выборе **Определено пользователем** необходимо будет задать аналитики в компании-получателе, щелкнув пункт меню **Аналитики получателя**.</span><span class="sxs-lookup"><span data-stu-id="765af-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="765af-193">Выберите исходные аналитики и финансовые аналитики и значения, которые используются в качестве источника исключения.</span><span class="sxs-lookup"><span data-stu-id="765af-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="765af-194">Обработка проводок исключений</span><span class="sxs-lookup"><span data-stu-id="765af-194">Process elimination transactions</span></span>
<span data-ttu-id="765af-195">Существует два способа обработки проводок исключения: в процессе интерактивной консолидации или путем создания журнала исключений и запуска процесса предложения исключений.</span><span class="sxs-lookup"><span data-stu-id="765af-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="765af-196">Этот раздел посвящен созданию журнала и выполнению процесса исключения.</span><span class="sxs-lookup"><span data-stu-id="765af-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="765af-197">В компании, определенной как компания для исключения, выберите **Журнал исключений** в модуле "Консолидации".</span><span class="sxs-lookup"><span data-stu-id="765af-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="765af-198">После выбора названия журнала нажмите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="765af-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="765af-199">Предложение можно выполнить, выбрав меню **Предложения**, затем выбрав **Предложение исключения**.</span><span class="sxs-lookup"><span data-stu-id="765af-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="765af-200">Выберите компанию, которая является источником консолидированных данных, затем выберите правило, которое необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="765af-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="765af-201">Введите дату начала, чтобы начать поиск сумм для списания, и конечную дату, чтобы завершить поиск по датам сумм исключения.</span><span class="sxs-lookup"><span data-stu-id="765af-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="765af-202">Поле **Дата разноски ГК** — это дата, используемая для разноски журнала в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="765af-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="765af-203">После нажатия кнопки **ОК** можно просмотреть суммы и разнести журнал.</span><span class="sxs-lookup"><span data-stu-id="765af-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




