---
title: Распределения по бухгалтерским счетам и записи в журнале для накладных с произвольным текстом
description: Распределения по бухгалтерским счетам используются для определения способа учета сумм, например дохода, налога или начислений в накладной с произвольным текстом, С каждой суммой, подлежащей учету при регистрации накладной с произвольным текстом в журнале, будут связаны одно или несколько распределений по бухгалтерским счетам,
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c3609ed396b543bb708ea36f308eee60976e66f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837185"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="b6839-104">Распределения по бухгалтерским счетам и записи в журнале для накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6839-105">Распределения по бухгалтерским счетам используются для определения способа учета сумм, например дохода, налога или начислений в накладной с произвольным текстом,</span><span class="sxs-lookup"><span data-stu-id="b6839-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="b6839-106">С каждой суммой, подлежащей учету при регистрации накладной с произвольным текстом в журнале, будут связаны одно или несколько распределений по бухгалтерским счетам,</span><span class="sxs-lookup"><span data-stu-id="b6839-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="b6839-107">Распределение по бухгалтерским счетам</span><span class="sxs-lookup"><span data-stu-id="b6839-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="b6839-108">Можно использовать следующие кнопки на странице "Накладная с произвольным текстом", чтобы просматривать и по возможности изменять распределения по бухгалтерским счетам для каждой суммы в накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="b6839-109">**Распределить суммы** — Просмотр и изменение распределений по бухгалтерским счетам для отдельной строки и любых дочерних строк, например для налогов и начислений.</span><span class="sxs-lookup"><span data-stu-id="b6839-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="b6839-110">Вы можете также просмотреть и изменить распределения по бухгалтерским счетам для дочерней строки непосредственно со страницы "Налоговые проводки" или "Проводки по накладным расходам".</span><span class="sxs-lookup"><span data-stu-id="b6839-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="b6839-111">Измените суммы в заголовке накладной с произвольным текстом, например начисления или суммы округления валюты.</span><span class="sxs-lookup"><span data-stu-id="b6839-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="b6839-112">Измените сумма в строках в накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="b6839-113">**Просмотр распределений** — Просмотр распределений по бухгалтерским счетам для всех строк документа.</span><span class="sxs-lookup"><span data-stu-id="b6839-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="b6839-114">В этом представлении изменять распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="b6839-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="b6839-115">Просмотрите суммы заголовка и строк.</span><span class="sxs-lookup"><span data-stu-id="b6839-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="b6839-116">Распределение сумм</span><span class="sxs-lookup"><span data-stu-id="b6839-116">Distributing amounts</span></span>
<span data-ttu-id="b6839-117">При вводе накладной с произвольным текстом каждая сумма будет распределяться следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b6839-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6839-118">Тип денежной суммы</span><span class="sxs-lookup"><span data-stu-id="b6839-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="b6839-119">Источник отображения счета ГК</span><span class="sxs-lookup"><span data-stu-id="b6839-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="b6839-120">Порядок приоритетов, определяющий финансовую аналитику, отображаемую по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b6839-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6839-121">Строка накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="b6839-122">Счет книги учета для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b6839-123">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="b6839-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b6839-124">Если счет ГК не является счетом распределения, используйте шаблон финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-125">Используйте значения финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-126">Используйте значения финансовой аналитики по умолчанию из счета учета на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="b6839-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6839-127">Строка накладной с произвольным текстом для комбинации кода основного средства и модели стоимости</span><span class="sxs-lookup"><span data-stu-id="b6839-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6839-128"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="b6839-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6839-129">Счетом ГК для строки накладной с произвольным текстом будет счет выбытия основного средства.</span><span class="sxs-lookup"><span data-stu-id="b6839-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="b6839-130">Счет книги учета для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b6839-131">Используйте значения финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-132">Используйте значения финансовой аналитики по умолчанию из счета учета на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="b6839-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6839-133">Сумма скидки в накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="b6839-134">Счет ГК для поля скидки клиента на странице "Скидки по оплате".</span><span class="sxs-lookup"><span data-stu-id="b6839-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b6839-135">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="b6839-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b6839-136">Если счет ГК не является счетом распределения, используйте шаблон финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-137">Используйте значения финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-138">Используйте значения финансовой аналитики по умолчанию из счета учета на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="b6839-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6839-139">Сумма налогов в накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="b6839-140">Поле "Исходящий налог" на странице "Группы разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="b6839-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b6839-141">Используйте финансовые аналитики, определенные для суммы строки накладной с произвольным текстом, или распределения для суммы строки начисления.</span><span class="sxs-lookup"><span data-stu-id="b6839-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="b6839-142">Используйте значения финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-143">Используйте значения финансовой аналитики по умолчанию из счета учета на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="b6839-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6839-144">Сумма строки начисления в накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="b6839-145">Поле "Кредитовый счет" на странице "Код накладных расходов".</span><span class="sxs-lookup"><span data-stu-id="b6839-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b6839-146">Если счет ГК - это счет распределения, используйте значение по умолчанию из его определения.</span><span class="sxs-lookup"><span data-stu-id="b6839-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b6839-147">Если счет ГК не является счетом распределения, используйте шаблон финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-148">Используйте значения финансовой аналитики по умолчанию для строки накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b6839-149">Используйте значения финансовой аналитики по умолчанию из счета учета на странице "План счетов".</span><span class="sxs-lookup"><span data-stu-id="b6839-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="b6839-150">Распределение налогов</span><span class="sxs-lookup"><span data-stu-id="b6839-150">Distributing taxes</span></span>
<span data-ttu-id="b6839-151">До расчета налогов создать для них распределения по бухгалтерским счетам нельзя.</span><span class="sxs-lookup"><span data-stu-id="b6839-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="b6839-152">Чтобы рассчитать налоги, необходимо на странице "Накладная с произвольным текстом" выполнить одну из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b6839-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="b6839-153">Просмотрите налог.</span><span class="sxs-lookup"><span data-stu-id="b6839-153">View the sales tax.</span></span>
-   <span data-ttu-id="b6839-154">Просмотрите итоговую сумму по накладной.</span><span class="sxs-lookup"><span data-stu-id="b6839-154">View the invoice total.</span></span>
-   <span data-ttu-id="b6839-155">Просмотрите движение денежных средств.</span><span class="sxs-lookup"><span data-stu-id="b6839-155">View the cash flow.</span></span>
-   <span data-ttu-id="b6839-156">Просмотрите распределения по бухгалтерским счетам для всей накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="b6839-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="b6839-157">Просмотрите журнал субкниги.</span><span class="sxs-lookup"><span data-stu-id="b6839-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="b6839-158">Журналы субкниги для накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="b6839-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="b6839-159">Перед разноской накладной с произвольным текстом можно просмотреть запись полного учета накладной, в которую включены дебетовые и кредитовые операции, и убедиться, что накладная будет разнесена на нужные счета.</span><span class="sxs-lookup"><span data-stu-id="b6839-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="b6839-160">Это представление записи полного учета называется журналом субкниги.</span><span class="sxs-lookup"><span data-stu-id="b6839-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="b6839-161">Нельзя изменить неправильную запись в журнале субкниги при ее предварительном просмотре до регистрации накладной с произвольным текстом в журнале.</span><span class="sxs-lookup"><span data-stu-id="b6839-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="b6839-162">Вместо этого необходимо изменить распределения по бухгалтерским счетам или профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="b6839-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="b6839-163">Распределения по бухгалтерским счетам используются для определения одной из сторон записи по счету, дебетовой или кредитовой.</span><span class="sxs-lookup"><span data-stu-id="b6839-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="b6839-164">Корректирующая запись для счета журнала субкниги создается из профилей разноски, например, из счета клиента или налога.</span><span class="sxs-lookup"><span data-stu-id="b6839-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]