---
title: Типы разноски аренды
description: В этой теме описываются типы разноски, которые используются для проводок по аренде активов.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ddc229f3ab8e048390f27503e2c6c26bd1a6f24f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841149"
---
# <a name="lease-posting-types"></a><span data-ttu-id="9844f-103">Типы разноски аренды</span><span class="sxs-lookup"><span data-stu-id="9844f-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9844f-104">В этой теме описываются типы разноски, которые используются для проводок по аренде активов.</span><span class="sxs-lookup"><span data-stu-id="9844f-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="9844f-105">Арендуемый актив</span><span class="sxs-lookup"><span data-stu-id="9844f-105">Lease asset</span></span>

<span data-ttu-id="9844f-106">Счет связан с активом в форме права пользования (ФПП).</span><span class="sxs-lookup"><span data-stu-id="9844f-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="9844f-107">Этот счет дебетуется, когда аренда первоначально распознается в соответствии с новыми стандартами учета аренды, тема 842 кодификации стандартов учета (ASC 842) и международным стандартом финансовой отчетности 16 (МСФО 16).</span><span class="sxs-lookup"><span data-stu-id="9844f-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="9844f-108">Для измененной аренды этот счет может либо дебетоваться, либо кредитоваться, в зависимости от того, увеличивается или уменьшается обязательство по аренде в результате изменения.</span><span class="sxs-lookup"><span data-stu-id="9844f-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="9844f-109">**Пример записей журнала:** первоначальное распознавание</span><span class="sxs-lookup"><span data-stu-id="9844f-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="9844f-110">**Дебет:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="9844f-111">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="9844f-112">Арендное обязательство</span><span class="sxs-lookup"><span data-stu-id="9844f-112">Lease liability</span></span>

<span data-ttu-id="9844f-113">Счет связывается с обязательством по аренде, которое генерируется, когда платежи дисконтируются в соответствии с новыми стандартами МСФО 16 и ASC 842.</span><span class="sxs-lookup"><span data-stu-id="9844f-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="9844f-114">Этот счет кредитуется, когда аренда первоначально распознается в соответствии с новыми стандартами.</span><span class="sxs-lookup"><span data-stu-id="9844f-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="9844f-115">Он дебетуется для платежей аренды и кредитуется для начислений процентов.</span><span class="sxs-lookup"><span data-stu-id="9844f-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="9844f-116">**Пример записей журнала:** первоначальное распознавание</span><span class="sxs-lookup"><span data-stu-id="9844f-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="9844f-117">**Дебет:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="9844f-118">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="9844f-119">**Пример записей журнала:** начисление процентов</span><span class="sxs-lookup"><span data-stu-id="9844f-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="9844f-120">**Дебет:** расходы на выплату процентов XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="9844f-121">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="9844f-122">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="9844f-123">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="9844f-124">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="9844f-125">Краткосрочное арендное обязательство</span><span class="sxs-lookup"><span data-stu-id="9844f-125">Short-term lease liability</span></span>

<span data-ttu-id="9844f-126">Счет связан с обязательством по краткосрочной аренде при разноске записи журнала изменения классификации обязательств по краткосрочной аренде.</span><span class="sxs-lookup"><span data-stu-id="9844f-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="9844f-127">Этот счет кредитуется для краткосрочного обязательства из графика амортизации в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="9844f-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="9844f-128">Однако та же сумма дебетуется в первый день следующего месяца.</span><span class="sxs-lookup"><span data-stu-id="9844f-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="9844f-129">**Пример записей журнала:** переопределение обязательств по краткосрочной аренде</span><span class="sxs-lookup"><span data-stu-id="9844f-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="9844f-130">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="9844f-131">**Кредит:** краткосрочное арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="9844f-132">**Дебет:** краткосрочное арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="9844f-133">**Кредит:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="9844f-134">Расходы на амортизацию</span><span class="sxs-lookup"><span data-stu-id="9844f-134">Depreciation expense</span></span>

<span data-ttu-id="9844f-135">Счет связан с расходами, относящимися к амортизации актива ФПП по МСФО 16, ASC 842 и финансовой аренде по IAS 17 и ASC 840.</span><span class="sxs-lookup"><span data-stu-id="9844f-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="9844f-136">Этот счет дебетуется, когда актив ФПП амортизируется каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="9844f-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="9844f-137">**Пример записей журнала:** начисление амортизации</span><span class="sxs-lookup"><span data-stu-id="9844f-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="9844f-138">**Дебет:** расходы на амортизацию XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="9844f-139">**Кредит:** накопленная амортизация XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="9844f-140">Прибыли/убытки от изменения аренды</span><span class="sxs-lookup"><span data-stu-id="9844f-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="9844f-141">Счет связан с любыми прибылями или убытками, возникшими в результате изменений аренды.</span><span class="sxs-lookup"><span data-stu-id="9844f-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="9844f-142">При изменении аренды может возникнуть прибыль в аренде, если изменение снижает обязательства по аренде на сумму, превышающую учетную стоимость для актива ФПП.</span><span class="sxs-lookup"><span data-stu-id="9844f-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="9844f-143">Например, арендная плата имеет текущую учетную стоимость арендного обязательства 150 000 долларов США и учетную стоимость актива ФПП 100 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="9844f-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="9844f-144">Аренда изменяется, и это изменение создает новую текущую стоимость минимальных арендных платежей будущих периодов (PVFMLP) из 40 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="9844f-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="9844f-145">Таким образом, арендное обязательство будет дебетоваться на 110 000 долларов США (150 000 – 40 000 долларов США).</span><span class="sxs-lookup"><span data-stu-id="9844f-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="9844f-146">Поскольку актив ФПП стоит только 100 000 долларов США, уменьшение на 110 000 долларов США уменьшит актив ниже 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="9844f-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="9844f-147">Таким образом, в руководстве по учету указано, что остаток должен быть отнесен на счет прибылей.</span><span class="sxs-lookup"><span data-stu-id="9844f-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="9844f-148">В этом случае окончательная запись журнала будет дебетом обязательства по аренде на 110 000 долларов США, кредита на аренду актива на 100 000 долларов США и кредит счет прибылей на 10 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="9844f-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="9844f-149">**Пример записей журнала:** изменение аренды</span><span class="sxs-lookup"><span data-stu-id="9844f-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="9844f-150">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="9844f-151">**Кредит:** актив аренды XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="9844f-152">**Кредит:** прибыль XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="9844f-153">Накопленная амортизация</span><span class="sxs-lookup"><span data-stu-id="9844f-153">Accumulated depreciation</span></span>

<span data-ttu-id="9844f-154">Счет связан с балансирующим счетом актива ФПП.</span><span class="sxs-lookup"><span data-stu-id="9844f-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="9844f-155">Этот счет кредитуется при разноске расходов на амортизацию.</span><span class="sxs-lookup"><span data-stu-id="9844f-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="9844f-156">**Пример записей журнала:** начисление амортизации</span><span class="sxs-lookup"><span data-stu-id="9844f-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="9844f-157">**Дебет:** расходы на амортизацию XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="9844f-158">**Кредит:** накопленная амортизация XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="9844f-159">Переменный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-159">Variable payment</span></span>

<span data-ttu-id="9844f-160">Счет связан с переменными платежами аренды, которые производятся при переоценке индекса при аренде ASC 842, ASC 840 и IAS 17.</span><span class="sxs-lookup"><span data-stu-id="9844f-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="9844f-161">В графике арендных платежей переменные платежи включаются в столбец **Переменный платеж**.</span><span class="sxs-lookup"><span data-stu-id="9844f-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="9844f-162">Этот счет дебетуется, когда создается накладная для строки графика оплаты, которая содержит переменный платеж.</span><span class="sxs-lookup"><span data-stu-id="9844f-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="9844f-163">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="9844f-164">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="9844f-165">**Дебет:** переменный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="9844f-166">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="9844f-167">Актив отложенной ренты (обязательство)</span><span class="sxs-lookup"><span data-stu-id="9844f-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="9844f-168">Счет связан с активом отложенной ренты или обязательством, производимым арендой с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="9844f-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="9844f-169">Этот счет дебетуется, когда накладная разнесена по аренде с обработкой отложенной ренты, если сумма арендного платежа превышает прямолинейные расходы по аренде для периода.</span><span class="sxs-lookup"><span data-stu-id="9844f-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="9844f-170">Он кредитуется, если арендный платеж меньше, чем прямолинейный расход по аренде за период.</span><span class="sxs-lookup"><span data-stu-id="9844f-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="9844f-171">**Пример записей журнала:** арендный платеж (аренда с обработкой отложенной ренты)</span><span class="sxs-lookup"><span data-stu-id="9844f-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="9844f-172">**Дебет:** расходы по аренде XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="9844f-173">**Кредит:** актив отложенной ренты XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="9844f-174">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="9844f-175">Расходы по аренде</span><span class="sxs-lookup"><span data-stu-id="9844f-175">Lease expense</span></span>

<span data-ttu-id="9844f-176">Счет связывается с расходом аренды, если арендная плата классифицируется как аренда с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="9844f-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="9844f-177">Этот счет дебетуется, когда накладная разносится по аренде с обработкой отложенной ренты.</span><span class="sxs-lookup"><span data-stu-id="9844f-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="9844f-178">**Пример записей журнала:** арендный платеж (аренда с обработкой отложенной ренты)</span><span class="sxs-lookup"><span data-stu-id="9844f-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="9844f-179">**Дебет:** расходы по аренде XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="9844f-180">**Кредит:** актив отложенной ренты XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="9844f-181">**Кредит:** оплачивается поставщиком/арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="9844f-182">Расход в связи с обесценением</span><span class="sxs-lookup"><span data-stu-id="9844f-182">Impairment expense</span></span>

<span data-ttu-id="9844f-183">Счет разносится тогда, когда аренда была обесценена.</span><span class="sxs-lookup"><span data-stu-id="9844f-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="9844f-184">Этот счет дебетуется, в то время как счет актива ФПП напрямую кредитуется.</span><span class="sxs-lookup"><span data-stu-id="9844f-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="9844f-185">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="9844f-186">**Дебет:** расход в связи с обесценением XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="9844f-187">**Кредит:** актив ФПП XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="9844f-188">Арендный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-188">Lease payment</span></span>

<span data-ttu-id="9844f-189">Счет разносится, если параметр **Платеж поставщику** отключен.</span><span class="sxs-lookup"><span data-stu-id="9844f-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="9844f-190">Этот счет кредитуется вместо расчетов с поставщиками, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="9844f-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="9844f-191">**Пример записей журнала:** арендный платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="9844f-192">**Дебет:** арендное обязательство XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="9844f-193">**Кредит:** арендный платеж XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="9844f-194">Разноски типов расходов</span><span class="sxs-lookup"><span data-stu-id="9844f-194">Expense type postings</span></span>

<span data-ttu-id="9844f-195">Счет, выбранный для каждого типа расходов, дебетуется при создании платежа для этого типа расходов.</span><span class="sxs-lookup"><span data-stu-id="9844f-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="9844f-196">Например, счет, указанный для типа расходов **Страховка**, дебетуется каждый раз, когда создается запись журнала накладных или платежей из графика затрат по осуществлению аренды для страховых расходов.</span><span class="sxs-lookup"><span data-stu-id="9844f-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="9844f-197">**Пример записей журнала:** страховой платеж</span><span class="sxs-lookup"><span data-stu-id="9844f-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="9844f-198">**Дебет:** счет типа расходов на страхование XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="9844f-199">**Кредит:** корр. счет XXX</span><span class="sxs-lookup"><span data-stu-id="9844f-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="9844f-200">Корр. счет выбирается на уровне аренды в строках графика оплаты затрат по осуществлению аренды.</span><span class="sxs-lookup"><span data-stu-id="9844f-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="9844f-201">Этот корр. счет может быть связан с поставщиком или со счетом книги учета.</span><span class="sxs-lookup"><span data-stu-id="9844f-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
