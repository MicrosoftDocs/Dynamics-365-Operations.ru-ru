---
title: Типы разноски аренды
description: В этой теме описываются типы разноски, которые используются для проводок по аренде активов.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881140"
---
# <a name="lease-posting-types"></a><span data-ttu-id="105c6-103">Типы разноски аренды</span><span class="sxs-lookup"><span data-stu-id="105c6-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="105c6-104">В этой теме описываются типы разноски, которые используются для проводок по аренде активов.</span><span class="sxs-lookup"><span data-stu-id="105c6-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="105c6-105">Арендуемый актив</span><span class="sxs-lookup"><span data-stu-id="105c6-105">Lease asset</span></span>

<span data-ttu-id="105c6-106">Счет связан с активом в форме права пользования (ФПП).</span><span class="sxs-lookup"><span data-stu-id="105c6-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="105c6-107">Этот счет дебетуется, когда аренда первоначально распознается в соответствии с новыми стандартами учета аренды, тема 842 кодификации стандартов учета (ASC 842) и международным стандартом финансовой отчетности 16 (МСФО 16).</span><span class="sxs-lookup"><span data-stu-id="105c6-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="105c6-108">Для измененной аренды этот счет может либо дебетоваться, либо кредитоваться, в зависимости от того, увеличивается или уменьшается обязательство по аренде в результате изменения.</span><span class="sxs-lookup"><span data-stu-id="105c6-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="105c6-109">**Пример записей журнала:** первоначальное распознавание</span><span class="sxs-lookup"><span data-stu-id="105c6-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="105c6-110">**Дебет:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="105c6-111">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="105c6-112">Арендное обязательство</span><span class="sxs-lookup"><span data-stu-id="105c6-112">Lease liability</span></span>

<span data-ttu-id="105c6-113">Счет связывается с обязательством по аренде, которое генерируется, когда платежи дисконтируются в соответствии с новыми стандартами МСФО 16 и ASC 842.</span><span class="sxs-lookup"><span data-stu-id="105c6-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="105c6-114">Этот счет кредитуется, когда аренда первоначально распознается в соответствии с новыми стандартами.</span><span class="sxs-lookup"><span data-stu-id="105c6-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="105c6-115">Он дебетуется для платежей аренды и кредитуется для начислений процентов.</span><span class="sxs-lookup"><span data-stu-id="105c6-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="105c6-116">**Пример записей журнала:** первоначальное распознавание</span><span class="sxs-lookup"><span data-stu-id="105c6-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="105c6-117">**Дебет:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="105c6-118">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="105c6-119">**Пример записей журнала:** начисление процентов</span><span class="sxs-lookup"><span data-stu-id="105c6-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="105c6-120">**Дебет:** расходы на выплату процентов XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="105c6-121">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="105c6-122">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="105c6-123">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="105c6-124">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="105c6-125">Краткосрочное арендное обязательство</span><span class="sxs-lookup"><span data-stu-id="105c6-125">Short-term lease liability</span></span>

<span data-ttu-id="105c6-126">Счет связан с обязательством по краткосрочной аренде при разноске записи журнала изменения классификации обязательств по краткосрочной аренде.</span><span class="sxs-lookup"><span data-stu-id="105c6-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="105c6-127">Этот счет кредитуется для краткосрочного обязательства из графика амортизации в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="105c6-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="105c6-128">Однако та же сумма дебетуется в первый день следующего месяца.</span><span class="sxs-lookup"><span data-stu-id="105c6-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="105c6-129">**Пример записей журнала:** переопределение обязательств по краткосрочной аренде</span><span class="sxs-lookup"><span data-stu-id="105c6-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="105c6-130">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="105c6-131">**Кредит:** краткосрочное арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="105c6-132">**Дебет:** краткосрочное арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="105c6-133">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="105c6-134">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="105c6-134">Depreciation expense</span></span>

<span data-ttu-id="105c6-135">Счет связан с расходами, относящимися к амортизации актива ФПП по МСФО 16, ASC 842 и финансовой аренде по IAS 17 и ASC 840.</span><span class="sxs-lookup"><span data-stu-id="105c6-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="105c6-136">Этот счет дебетуется, когда актив ФПП амортизируется каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="105c6-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="105c6-137">**Пример записей журнала:** начисление амортизации</span><span class="sxs-lookup"><span data-stu-id="105c6-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="105c6-138">**Дебет:** расходы на амортизацию XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="105c6-139">**Кредит:** накопленная амортизация XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="105c6-140">Прибыли/убытки от изменения аренды</span><span class="sxs-lookup"><span data-stu-id="105c6-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="105c6-141">Счет связан с любыми прибылями или убытками, возникшими в результате изменений аренды.</span><span class="sxs-lookup"><span data-stu-id="105c6-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="105c6-142">При изменении аренды может возникнуть прибыль в аренде, если изменение снижает обязательства по аренде на сумму, превышающую учетную стоимость для актива ФПП.</span><span class="sxs-lookup"><span data-stu-id="105c6-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="105c6-143">Например, арендная плата имеет текущую учетную стоимость арендного обязательства 150 000 долларов США и учетную стоимость актива ФПП 100 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="105c6-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="105c6-144">Аренда изменяется, и это изменение создает новую текущую стоимость минимальных арендных платежей будущих периодов (PVFMLP) из 40 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="105c6-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="105c6-145">Таким образом, арендное обязательство будет дебетоваться на 110 000 долларов США (150 000 – 40 000 долларов США).</span><span class="sxs-lookup"><span data-stu-id="105c6-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="105c6-146">Поскольку актив ФПП стоит только 100 000 долларов США, уменьшение на 110 000 долларов США уменьшит актив ниже 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="105c6-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="105c6-147">Таким образом, в руководстве по учету указано, что остаток должен быть отнесен на счет прибылей.</span><span class="sxs-lookup"><span data-stu-id="105c6-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="105c6-148">В этом случае окончательная запись журнала будет дебетом обязательства по аренде на 110 000 долларов США, кредита на аренду актива на 100 000 долларов США и кредит счет прибылей на 10 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="105c6-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="105c6-149">**Пример записей журнала:** изменение аренды</span><span class="sxs-lookup"><span data-stu-id="105c6-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="105c6-150">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="105c6-151">**Кредит:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="105c6-152">**Кредит:** прибыль XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="105c6-153">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="105c6-153">Accumulated depreciation</span></span>

<span data-ttu-id="105c6-154">Счет связан с балансирующим счетом актива ФПП.</span><span class="sxs-lookup"><span data-stu-id="105c6-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="105c6-155">Этот счет кредитуется при разноске расходов на амортизацию.</span><span class="sxs-lookup"><span data-stu-id="105c6-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="105c6-156">**Пример записей журнала:** начисление амортизации</span><span class="sxs-lookup"><span data-stu-id="105c6-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="105c6-157">**Дебет:** расходы на амортизацию XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="105c6-158">**Кредит:** накопленная амортизация XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="105c6-159">Переменный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-159">Variable payment</span></span>

<span data-ttu-id="105c6-160">Счет связан с переменными платежами аренды, которые производятся при переоценке индекса при аренде ASC 842, ASC 840 и IAS 17.</span><span class="sxs-lookup"><span data-stu-id="105c6-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="105c6-161">В графике арендных платежей переменные платежи включаются в столбец **Переменный платеж**.</span><span class="sxs-lookup"><span data-stu-id="105c6-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="105c6-162">Этот счет дебетуется, когда создается накладная для строки графика оплаты, которая содержит переменный платеж.</span><span class="sxs-lookup"><span data-stu-id="105c6-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="105c6-163">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="105c6-164">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="105c6-165">**Дебет:** переменный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="105c6-166">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="105c6-167">Актив отложенной ренты (обязательство)</span><span class="sxs-lookup"><span data-stu-id="105c6-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="105c6-168">Счет связан с активом отложенной ренты или обязательством, производимым арендой с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="105c6-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="105c6-169">Этот счет дебетуется, когда накладная разнесена по аренде с обработкой отложенной ренты, если сумма арендного платежа превышает прямолинейные расходы по аренде для периода.</span><span class="sxs-lookup"><span data-stu-id="105c6-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="105c6-170">Он кредитуется, если арендный платеж меньше, чем прямолинейный расход по аренде за период.</span><span class="sxs-lookup"><span data-stu-id="105c6-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="105c6-171">**Пример записей журнала:** арендный платеж (аренда с обработкой отложенной ренты)</span><span class="sxs-lookup"><span data-stu-id="105c6-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="105c6-172">**Дебет:** расходы по аренде XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="105c6-173">**Кредит:** актив отложенной ренты XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="105c6-174">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="105c6-175">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="105c6-175">Lease expense</span></span>

<span data-ttu-id="105c6-176">Счет связывается с расходом аренды, если арендная плата классифицируется как аренда с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="105c6-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="105c6-177">Этот счет дебетуется, когда накладная разносится по аренде с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="105c6-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="105c6-178">**Пример записей журнала:** арендный платеж (аренда с обработкой отложенной ренты)</span><span class="sxs-lookup"><span data-stu-id="105c6-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="105c6-179">**Дебет:** расходы по аренде XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="105c6-180">**Кредит:** актив отложенной ренты XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="105c6-181">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="105c6-182">Расход в связи с обесценением</span><span class="sxs-lookup"><span data-stu-id="105c6-182">Impairment expense</span></span>

<span data-ttu-id="105c6-183">Счет разносится тогда, когда аренда была обесценена.</span><span class="sxs-lookup"><span data-stu-id="105c6-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="105c6-184">Этот счет дебетуется, в то время как счет актива ФПП напрямую кредитуется.</span><span class="sxs-lookup"><span data-stu-id="105c6-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="105c6-185">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="105c6-186">**Дебет:** расход в связи с обесценением XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="105c6-187">**Кредит:** актив ФПП XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="105c6-188">Арендный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-188">Lease payment</span></span>

<span data-ttu-id="105c6-189">Счет разносится, если параметр **Платеж поставщику** отключен.</span><span class="sxs-lookup"><span data-stu-id="105c6-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="105c6-190">Этот счет кредитуется вместо расчетов с поставщиками, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="105c6-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="105c6-191">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="105c6-192">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="105c6-193">**Кредит:** арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="105c6-194">Разноски типов расходов</span><span class="sxs-lookup"><span data-stu-id="105c6-194">Expense type postings</span></span>

<span data-ttu-id="105c6-195">Счет, выбранный для каждого типа расходов, дебетуется при создании платежа для этого типа расходов.</span><span class="sxs-lookup"><span data-stu-id="105c6-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="105c6-196">Например, счет, указанный для типа расходов **Страховка**, дебетуется каждый раз, когда создается запись журнала накладных или платежей из графика затрат по осуществлению аренды для страховых расходов.</span><span class="sxs-lookup"><span data-stu-id="105c6-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="105c6-197">**Пример записей журнала:** страховой платеж</span><span class="sxs-lookup"><span data-stu-id="105c6-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="105c6-198">**Дебет:** счет типа расходов на страхование XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="105c6-199">**Кредит:** корр. счет XXX</span><span class="sxs-lookup"><span data-stu-id="105c6-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="105c6-200">Корр. счет выбирается на уровне аренды в строках графика оплаты затрат по осуществлению аренды.</span><span class="sxs-lookup"><span data-stu-id="105c6-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="105c6-201">Этот корр. счет может быть связан с поставщиком или со счетом книги учета.</span><span class="sxs-lookup"><span data-stu-id="105c6-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
