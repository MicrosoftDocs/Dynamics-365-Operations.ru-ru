---
title: Переоценка валюты в компании консолидации
description: В этой теме рассматривается переоценка валюты в консолидированной компании.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212237"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="06071-103">Переоценка валюты в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="06071-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06071-104">Когда вы консолидируете данные от одной валюты учета к другим, вы должны по-прежнему выполнить переоценку валюты, если есть изменение в обменных курсах, чтобы ваши сальдо счета были правильно переоценены.</span><span class="sxs-lookup"><span data-stu-id="06071-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="06071-105">Когда вы первоначально консолидируете данные, используйте вкладку **Трансляция валюты**, чтобы выбрать начальные обменные курсы к для трансляции во время процесса консолидации.</span><span class="sxs-lookup"><span data-stu-id="06071-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="06071-106">После того как вписан новый обменный курс (например, в следующем месяце), вы должны переоценить сальдо счета.</span><span class="sxs-lookup"><span data-stu-id="06071-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="06071-107">Внереализационные прибыли или потери после этого обновляются соответственно, на основе нового обменного курса и даты.</span><span class="sxs-lookup"><span data-stu-id="06071-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="06071-108">Следующий пример иллюстрирует записи учета, которые созданы во время процесса.</span><span class="sxs-lookup"><span data-stu-id="06071-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="06071-109">Настройка компании</span><span class="sxs-lookup"><span data-stu-id="06071-109">Company setup</span></span>
-   <span data-ttu-id="06071-110">**Источник/действующая компания (USMF)** — доллары США (USD) использованы как валюта учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="06071-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="06071-111">**Консолидированная компания (CON)** — евро (EUR) использованы как валюта учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="06071-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="06071-112">**Реализованная прибыль** — счет учета 801500</span><span class="sxs-lookup"><span data-stu-id="06071-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="06071-113">**Реализованный убыток** — счет учета 801600</span><span class="sxs-lookup"><span data-stu-id="06071-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="06071-114">**Внереализационная прибыль** — счет учета 801600</span><span class="sxs-lookup"><span data-stu-id="06071-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="06071-115">**Внереализационный убыток** — счет учета 801400</span><span class="sxs-lookup"><span data-stu-id="06071-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="06071-116">Исходные проводки</span><span class="sxs-lookup"><span data-stu-id="06071-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="06071-117">Проводки денежных поступлений в USMF</span><span class="sxs-lookup"><span data-stu-id="06071-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="06071-118">Дата</span><span class="sxs-lookup"><span data-stu-id="06071-118">Date</span></span>       | <span data-ttu-id="06071-119">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="06071-119">Ledger account</span></span>               | <span data-ttu-id="06071-120">Валютное</span><span class="sxs-lookup"><span data-stu-id="06071-120">Currency</span></span> | <span data-ttu-id="06071-121">Cумма</span><span class="sxs-lookup"><span data-stu-id="06071-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="06071-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="06071-122">10/11/2015</span></span> | <span data-ttu-id="06071-123">110110 – Касса</span><span class="sxs-lookup"><span data-stu-id="06071-123">110110 – Cash</span></span>                | <span data-ttu-id="06071-124">американский доллар</span><span class="sxs-lookup"><span data-stu-id="06071-124">USD</span></span>      | <span data-ttu-id="06071-125">500</span><span class="sxs-lookup"><span data-stu-id="06071-125">500</span></span>    |
| <span data-ttu-id="06071-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="06071-126">10/11/2015</span></span> | <span data-ttu-id="06071-127">130100 – Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="06071-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="06071-128">американский доллар</span><span class="sxs-lookup"><span data-stu-id="06071-128">USD</span></span>      | <span data-ttu-id="06071-129">-500</span><span class="sxs-lookup"><span data-stu-id="06071-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="06071-130">Валютные курсы</span><span class="sxs-lookup"><span data-stu-id="06071-130">Exchange rates</span></span>

| <span data-ttu-id="06071-131">От валюты</span><span class="sxs-lookup"><span data-stu-id="06071-131">From currency</span></span> | <span data-ttu-id="06071-132">До валюты</span><span class="sxs-lookup"><span data-stu-id="06071-132">To currency</span></span> | <span data-ttu-id="06071-133">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="06071-133">Start date</span></span> | <span data-ttu-id="06071-134">Курс обмена</span><span class="sxs-lookup"><span data-stu-id="06071-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="06071-135">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-135">EUR</span></span>           | <span data-ttu-id="06071-136">американский доллар</span><span class="sxs-lookup"><span data-stu-id="06071-136">USD</span></span>         | <span data-ttu-id="06071-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="06071-137">10/1/2015</span></span>  | <span data-ttu-id="06071-138">200</span><span class="sxs-lookup"><span data-stu-id="06071-138">200</span></span>           |
| <span data-ttu-id="06071-139">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-139">EUR</span></span>           | <span data-ttu-id="06071-140">американский доллар</span><span class="sxs-lookup"><span data-stu-id="06071-140">USD</span></span>         | <span data-ttu-id="06071-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="06071-141">11/1/2015</span></span>  | <span data-ttu-id="06071-142">150</span><span class="sxs-lookup"><span data-stu-id="06071-142">150</span></span>           |
| <span data-ttu-id="06071-143">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-143">EUR</span></span>           | <span data-ttu-id="06071-144">американский доллар</span><span class="sxs-lookup"><span data-stu-id="06071-144">USD</span></span>         | <span data-ttu-id="06071-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="06071-145">12/1/2012</span></span>  | <span data-ttu-id="06071-146">100</span><span class="sxs-lookup"><span data-stu-id="06071-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="06071-147">Выполните консолидацию на октябрь 2015</span><span class="sxs-lookup"><span data-stu-id="06071-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="06071-148">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="06071-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="06071-149">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="06071-149">Ledger account</span></span> | <span data-ttu-id="06071-150">Валютное</span><span class="sxs-lookup"><span data-stu-id="06071-150">Currency</span></span> | <span data-ttu-id="06071-151">Cумма</span><span class="sxs-lookup"><span data-stu-id="06071-151">Amount</span></span> | <span data-ttu-id="06071-152">Расчет</span><span class="sxs-lookup"><span data-stu-id="06071-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="06071-153">110110</span><span class="sxs-lookup"><span data-stu-id="06071-153">110110</span></span>         | <span data-ttu-id="06071-154">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-154">EUR</span></span>      | <span data-ttu-id="06071-155">250</span><span class="sxs-lookup"><span data-stu-id="06071-155">250</span></span>    | <span data-ttu-id="06071-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="06071-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="06071-157">130100</span><span class="sxs-lookup"><span data-stu-id="06071-157">130100</span></span>         | <span data-ttu-id="06071-158">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-158">EUR</span></span>      | <span data-ttu-id="06071-159">-250</span><span class="sxs-lookup"><span data-stu-id="06071-159">-250</span></span>   | <span data-ttu-id="06071-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="06071-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="06071-161">Выполните переоценку валюты для счета, начиная с 1-ого октября 2015 до 30-ого ноября 2015</span><span class="sxs-lookup"><span data-stu-id="06071-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="06071-162">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="06071-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="06071-163">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="06071-163">Ledger account</span></span> | <span data-ttu-id="06071-164">Валютное</span><span class="sxs-lookup"><span data-stu-id="06071-164">Currency</span></span> | <span data-ttu-id="06071-165">Cумма</span><span class="sxs-lookup"><span data-stu-id="06071-165">Amount</span></span>  | <span data-ttu-id="06071-166">Расчет</span><span class="sxs-lookup"><span data-stu-id="06071-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="06071-167">110110</span><span class="sxs-lookup"><span data-stu-id="06071-167">110110</span></span>         | <span data-ttu-id="06071-168">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-168">EUR</span></span>      | <span data-ttu-id="06071-169">333,33</span><span class="sxs-lookup"><span data-stu-id="06071-169">333.33</span></span>  | <span data-ttu-id="06071-170">Исходная сумма 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="06071-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="06071-171">130100</span><span class="sxs-lookup"><span data-stu-id="06071-171">130100</span></span>         | <span data-ttu-id="06071-172">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-172">EUR</span></span>      | <span data-ttu-id="06071-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="06071-173">-333.33</span></span> | <span data-ttu-id="06071-174">Исходная сумма -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="06071-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="06071-175">801400</span><span class="sxs-lookup"><span data-stu-id="06071-175">801400</span></span>         | <span data-ttu-id="06071-176">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-176">EUR</span></span>      | <span data-ttu-id="06071-177">83,33</span><span class="sxs-lookup"><span data-stu-id="06071-177">83.33</span></span>   | <span data-ttu-id="06071-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="06071-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="06071-179">801600</span><span class="sxs-lookup"><span data-stu-id="06071-179">801600</span></span>         | <span data-ttu-id="06071-180">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-180">EUR</span></span>      | <span data-ttu-id="06071-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="06071-181">-83.33</span></span>  | <span data-ttu-id="06071-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="06071-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="06071-183">Вы увидите дополнительные проводки для сумм в валюте отчетности.</span><span class="sxs-lookup"><span data-stu-id="06071-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="06071-184">Выполните переоценку валюты для счета, начиная с 1-ого октября 2015 до 31-ого декабря 2015</span><span class="sxs-lookup"><span data-stu-id="06071-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="06071-185">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="06071-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="06071-186">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="06071-186">Ledger account</span></span> | <span data-ttu-id="06071-187">Валютное</span><span class="sxs-lookup"><span data-stu-id="06071-187">Currency</span></span> | <span data-ttu-id="06071-188">Cумма</span><span class="sxs-lookup"><span data-stu-id="06071-188">Amount</span></span>  | <span data-ttu-id="06071-189">Расчет</span><span class="sxs-lookup"><span data-stu-id="06071-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="06071-190">110110</span><span class="sxs-lookup"><span data-stu-id="06071-190">110110</span></span>         | <span data-ttu-id="06071-191">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-191">EUR</span></span>      | <span data-ttu-id="06071-192">500,00</span><span class="sxs-lookup"><span data-stu-id="06071-192">500.00</span></span>  | <span data-ttu-id="06071-193">Исходная сумма 500 × 1</span><span class="sxs-lookup"><span data-stu-id="06071-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="06071-194">130100</span><span class="sxs-lookup"><span data-stu-id="06071-194">130100</span></span>         | <span data-ttu-id="06071-195">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-195">EUR</span></span>      | <span data-ttu-id="06071-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="06071-196">-500.00</span></span> | <span data-ttu-id="06071-197">Исходная сумма -500 × 1</span><span class="sxs-lookup"><span data-stu-id="06071-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="06071-198">801400</span><span class="sxs-lookup"><span data-stu-id="06071-198">801400</span></span>         | <span data-ttu-id="06071-199">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-199">EUR</span></span>      | <span data-ttu-id="06071-200">250</span><span class="sxs-lookup"><span data-stu-id="06071-200">250</span></span>     | <span data-ttu-id="06071-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="06071-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="06071-202">801600</span><span class="sxs-lookup"><span data-stu-id="06071-202">801600</span></span>         | <span data-ttu-id="06071-203">Евро</span><span class="sxs-lookup"><span data-stu-id="06071-203">EUR</span></span>      | <span data-ttu-id="06071-204">-250</span><span class="sxs-lookup"><span data-stu-id="06071-204">-250</span></span>    | <span data-ttu-id="06071-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="06071-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]