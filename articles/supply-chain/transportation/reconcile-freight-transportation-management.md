---
title: Выверка фрахта в модуле "Управление транспортировкой"
description: В этой теме описывается процесс выверки фрахта.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af7bbb500de25e0a796147fae42cd7d943be9df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205234"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="df327-103">Выверка фрахта в модуле "Управление транспортировкой"</span><span class="sxs-lookup"><span data-stu-id="df327-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df327-104">В этой теме описывается процесс выверки фрахта.</span><span class="sxs-lookup"><span data-stu-id="df327-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="df327-105">Выверку фрахта можно выполнить вручную или настроить для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="df327-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="df327-106">Чтобы использовать автоматическую выверку фрахта, необходимо настроить шаблон аудита, в котором можно определить критерии, определяющие, какие векселя фрахта будут сопоставляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="df327-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="df327-107">Процесс выверки фрахта</span><span class="sxs-lookup"><span data-stu-id="df327-107">The freight reconciliation process</span></span>

<span data-ttu-id="df327-108">Фрахтовые ставки рассчитываются механизмом ставок, связанным с соответствующим перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="df327-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="df327-109">При подтверждении загрузки создается вексель фрахта и в него передаются фрахтовые ставки.</span><span class="sxs-lookup"><span data-stu-id="df327-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="df327-110">Фрахтовые ставки распределяются как накладные расходы для соответствующего документа-источника (заказ на покупку, заказ на продажу или заказ на перемещение) в зависимости от настройки, используемой для стандартного процесса выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="df327-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="df327-111">Процесс выверки фрахта (который также называется процессом сопоставления) можно запустить сразу после поступления накладной фрахта от перевозчика.</span><span class="sxs-lookup"><span data-stu-id="df327-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="df327-112">Накладную можно получить в электронном или бумажном формате.</span><span class="sxs-lookup"><span data-stu-id="df327-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="df327-113">Если накладная поступает в бумажном формате, можно создать электронную накладную с помощью векселя фрахта в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="df327-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="df327-114">[![Процесс выверки фрахта](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="df327-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="df327-115">Выверка вручную</span><span class="sxs-lookup"><span data-stu-id="df327-115">Manual reconciliation</span></span>

<span data-ttu-id="df327-116">Если фрахт выверяется вручную, необходимо сопоставить каждую строку накладной со строкой или строками векселя фрахта для загрузки, по которой выставляется накладная.</span><span class="sxs-lookup"><span data-stu-id="df327-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="df327-117">Это сопоставление выполняется на странице **Сопоставление векселя фрахта с накладной**.</span><span class="sxs-lookup"><span data-stu-id="df327-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="df327-118">Если сумма в строке накладной не соответствует сумме векселя фрахта, необходимо выбрать причину для разницы выверки.</span><span class="sxs-lookup"><span data-stu-id="df327-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="df327-119">Если существует несколько причин для выверки, можно разделить несоответствующую сумму между ними.</span><span class="sxs-lookup"><span data-stu-id="df327-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="df327-120">Причина выверки определяет способ разноски сумм разницы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="df327-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="df327-121">При учитывается выверка всей суммы накладной, она направляется на утверждение, после чего выполняется разноска журнала.</span><span class="sxs-lookup"><span data-stu-id="df327-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="df327-122">В следующем примере показано, как создать накладную фрахта и выполнить выверку фрахта.</span><span class="sxs-lookup"><span data-stu-id="df327-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="df327-123">[![Задачи выверки фрахта](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="df327-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="df327-124">Автоматическая выверка</span><span class="sxs-lookup"><span data-stu-id="df327-124">Automatic reconciliation</span></span>

<span data-ttu-id="df327-125">Чтобы использовать автоматическую выверку, необходимо указать расписание для выверки, а также накладные и перевозчиков для использования.</span><span class="sxs-lookup"><span data-stu-id="df327-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="df327-126">Сопоставление строк накладной и векселей фрахта осуществляется в соответствии с настройкой шаблона аудита и типом векселя фрахта.</span><span class="sxs-lookup"><span data-stu-id="df327-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="df327-127">После выполнения автоматической выверки необходимо обработать все накладные, которые система не может сопоставить.</span><span class="sxs-lookup"><span data-stu-id="df327-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="df327-128">Затем необходимо обработать эти накладные вручную, перед разноской всех накладных для платежа.</span><span class="sxs-lookup"><span data-stu-id="df327-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="df327-129">Сопоставление счетов фрахта с накладными по фрахту с использованием автоматической или ручной выверки</span><span class="sxs-lookup"><span data-stu-id="df327-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="df327-130">*Сопоставление* — это процесс поиска счетов фрахта, соответствующих каждой накладной по фрахту.</span><span class="sxs-lookup"><span data-stu-id="df327-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="df327-131">Это может быть выполнено путем сопоставления строк накладной по одной (ручное сопоставление) или путем сопоставления всех доступных накладных одновременно (автоматическое сопоставление).</span><span class="sxs-lookup"><span data-stu-id="df327-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="df327-132">Автоматическое сопоставление</span><span class="sxs-lookup"><span data-stu-id="df327-132">Auto matching</span></span>

<span data-ttu-id="df327-133">При сопоставлении нескольких накладных по фрахту одному счету фрахта процесс автоматического сопоставления будет работать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="df327-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="df327-134">Все несопоставленные накладные по фрахту сортируются по сумме, начиная с наибольшей суммы.</span><span class="sxs-lookup"><span data-stu-id="df327-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="df327-135">Накладные по фрахту сопоставляются по одной до тех пор, пока на счете фрахта остается положительная сумма.</span><span class="sxs-lookup"><span data-stu-id="df327-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="df327-136">В зависимости от настройки мастера аудита и оставшейся суммы по накладным по фрахту устанавливается сумма остатка.</span><span class="sxs-lookup"><span data-stu-id="df327-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="df327-137">Сопоставление вручную</span><span class="sxs-lookup"><span data-stu-id="df327-137">Manual matching</span></span>

<span data-ttu-id="df327-138">Все счета по фрахту с положительными суммами будут доступны для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="df327-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="df327-139">Аналогично автоматическому сопоставлению, пользователь может только сопоставлять накладные по фрахту с отрицательными суммами со счетами по фрахту без полного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="df327-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="df327-140">Пример</span><span class="sxs-lookup"><span data-stu-id="df327-140">Example</span></span>

<span data-ttu-id="df327-141">Предположим, имеется счет фрахта (FB) на сумму 1500, и вы создали три накладных по фрахту для этого счета фрахта с одной строкой накладной для каждой накладной со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="df327-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="df327-142">Первоначальный счет по фрахту (FB): сумма 1500</span><span class="sxs-lookup"><span data-stu-id="df327-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="df327-143">Накладная 1 (Inv1): сумма 1000</span><span class="sxs-lookup"><span data-stu-id="df327-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="df327-144">Накладная 2 (Inv2): сумма 600</span><span class="sxs-lookup"><span data-stu-id="df327-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="df327-145">Накладная 3 (Inv3): сумма –100</span><span class="sxs-lookup"><span data-stu-id="df327-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="df327-146">Результат автоматического сопоставления</span><span class="sxs-lookup"><span data-stu-id="df327-146">Automatic matching result</span></span>

<span data-ttu-id="df327-147">Автоматическое сопоставление будет выполняться в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="df327-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="df327-148">Сортировка всех накладных по фрахту по убыванию суммы: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="df327-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="df327-149">Сопоставление Inv1 с FB.</span><span class="sxs-lookup"><span data-stu-id="df327-149">Match Inv1 with FB.</span></span> <span data-ttu-id="df327-150">Inv1 имеет сопоставленную сумму 1000, а FB имеет оставшуюся сумму 500, поэтому статус установлен на *Частично сопоставлено*.</span><span class="sxs-lookup"><span data-stu-id="df327-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="df327-151">Сопоставление Inv2 с FB.</span><span class="sxs-lookup"><span data-stu-id="df327-151">Match Inv2 with FB.</span></span> <span data-ttu-id="df327-152">Inv2 имеет сопоставленную сумму 500, а FB имеет оставшуюся сумму 0, поэтому статус установлен на *Полностью сопоставлено*.</span><span class="sxs-lookup"><span data-stu-id="df327-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="df327-153">Так как FB теперь полностью сопоставлен, Inv3 не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="df327-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="df327-154">Результат сопоставления вручную</span><span class="sxs-lookup"><span data-stu-id="df327-154">Manual matching result</span></span>

<span data-ttu-id="df327-155">Для ручного сопоставления результаты изменяются в зависимости от порядка сопоставления, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="df327-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="df327-156">Ручное сопоставление, случай 1</span><span class="sxs-lookup"><span data-stu-id="df327-156">Manual matching case 1</span></span>

<span data-ttu-id="df327-157">Одним из способов ручного сопоставления в этом примере является продолжение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="df327-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="df327-158">Сопоставление FB с Inv1.</span><span class="sxs-lookup"><span data-stu-id="df327-158">Match FB with Inv1.</span></span> <span data-ttu-id="df327-159">FB имеет оставшуюся сумму 500, поэтому статус установлен на *Частично сопоставлено*.</span><span class="sxs-lookup"><span data-stu-id="df327-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="df327-160">Сопоставление Inv2 с FB.</span><span class="sxs-lookup"><span data-stu-id="df327-160">Match Inv2 with FB.</span></span> <span data-ttu-id="df327-161">Inv2 имеет сопоставленную сумму 500, а FB имеет оставшуюся сумму 0, поэтому статус установлен на *Полностью сопоставлено*.</span><span class="sxs-lookup"><span data-stu-id="df327-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="df327-162">При ручном сопоставлении Inv3 не будут обнаружено никаких несопоставленных счетов по фрахту.</span><span class="sxs-lookup"><span data-stu-id="df327-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="df327-163">Этот случай, в сущности, такой же, как и автоматическое сопоставление</span><span class="sxs-lookup"><span data-stu-id="df327-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="df327-164">Ручное сопоставление, случай 2</span><span class="sxs-lookup"><span data-stu-id="df327-164">Manual matching case 2</span></span>

<span data-ttu-id="df327-165">Другим способом ручного сопоставления в этом примере является продолжение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="df327-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="df327-166">Сопоставление Inv3 с FB.</span><span class="sxs-lookup"><span data-stu-id="df327-166">Match Inv3 with FB.</span></span> <span data-ttu-id="df327-167">Сейчас FB имеет оставшуюся сумму 1600, что есть сумма после вычитания отрицательных 100 из 1500.</span><span class="sxs-lookup"><span data-stu-id="df327-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="df327-168">Оба FB и Inv3 имеют сопоставленное количество –100.</span><span class="sxs-lookup"><span data-stu-id="df327-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="df327-169">Сопоставление Inv1 и Inv2 с FB одной за другой.</span><span class="sxs-lookup"><span data-stu-id="df327-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="df327-170">FB полностью сопоставлена.</span><span class="sxs-lookup"><span data-stu-id="df327-170">FB is fully matched.</span></span>

<span data-ttu-id="df327-171">Как показано в этом примере, сопоставление накладных по фрахту с отрицательными суммами должно выполняться только вручную.</span><span class="sxs-lookup"><span data-stu-id="df327-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="df327-172">Это гарантирует, что всегда можно будет сопоставить накладные по фрахту с отрицательными суммами со счетами по фрахту без полного сопоставления, поскольку это позволяет управлять последовательностью сопоставления.</span><span class="sxs-lookup"><span data-stu-id="df327-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]