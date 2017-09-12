---
title: "Переоценка валюты в компании консолидации"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="515af-102">Переоценка валюты в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="515af-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="515af-103">Когда вы консолидируете данные от одной валюты учета к другим, вы должны по-прежнему выполнить переоценку валюты, если есть изменение в обменных курсах, чтобы ваши сальдо счета были правильно переоценены.</span><span class="sxs-lookup"><span data-stu-id="515af-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="515af-104">Когда вы первоначально консолидируете данные, используйте вкладку **Трансляция валюты**, чтобы выбрать начальные обменные курсы к для трансляции во время процесса консолидации.</span><span class="sxs-lookup"><span data-stu-id="515af-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="515af-105">После того как вписан новый обменный курс (например, в следующем месяце), вы должны переоценить сальдо счета.</span><span class="sxs-lookup"><span data-stu-id="515af-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="515af-106">Внереализационные прибыли или потери после этого обновляются соответственно, на основе нового обменного курса и даты.</span><span class="sxs-lookup"><span data-stu-id="515af-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="515af-107">Следующий пример иллюстрирует записи учета, которые созданы во время процесса.</span><span class="sxs-lookup"><span data-stu-id="515af-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="515af-108">Настройка компании</span><span class="sxs-lookup"><span data-stu-id="515af-108">Company setup</span></span>
-   <span data-ttu-id="515af-109">**Источник/действующая компания (USMF)** — доллары США (USD) использованы как валюта учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="515af-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="515af-110">**Консолидированная компания (CON)** — евро (EUR) использованы как валюта учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="515af-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="515af-111">**Реализованная прибыль** — счет учета 801500</span><span class="sxs-lookup"><span data-stu-id="515af-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="515af-112">**Реализованный убыток** — счет учета 801600</span><span class="sxs-lookup"><span data-stu-id="515af-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="515af-113">**Внереализационная прибыль** — счет учета 801600</span><span class="sxs-lookup"><span data-stu-id="515af-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="515af-114">**Внереализационный убыток** — счет учета 801400</span><span class="sxs-lookup"><span data-stu-id="515af-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="515af-115">Исходные проводки</span><span class="sxs-lookup"><span data-stu-id="515af-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="515af-116">Проводки денежных поступлений в USMF</span><span class="sxs-lookup"><span data-stu-id="515af-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="515af-117">Дата</span><span class="sxs-lookup"><span data-stu-id="515af-117">Date</span></span>       | <span data-ttu-id="515af-118">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="515af-118">Ledger account</span></span>               | <span data-ttu-id="515af-119">Валютное</span><span class="sxs-lookup"><span data-stu-id="515af-119">Currency</span></span> | <span data-ttu-id="515af-120">Cумма</span><span class="sxs-lookup"><span data-stu-id="515af-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="515af-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="515af-121">10/11/2015</span></span> | <span data-ttu-id="515af-122">110110 – Касса</span><span class="sxs-lookup"><span data-stu-id="515af-122">110110 – Cash</span></span>                | <span data-ttu-id="515af-123">американский доллар</span><span class="sxs-lookup"><span data-stu-id="515af-123">USD</span></span>      | <span data-ttu-id="515af-124">500</span><span class="sxs-lookup"><span data-stu-id="515af-124">500</span></span>    |
| <span data-ttu-id="515af-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="515af-125">10/11/2015</span></span> | <span data-ttu-id="515af-126">130100 – Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="515af-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="515af-127">американский доллар</span><span class="sxs-lookup"><span data-stu-id="515af-127">USD</span></span>      | <span data-ttu-id="515af-128">-500</span><span class="sxs-lookup"><span data-stu-id="515af-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="515af-129">Валютные курсы</span><span class="sxs-lookup"><span data-stu-id="515af-129">Exchange rates</span></span>
| <span data-ttu-id="515af-130">От валюты</span><span class="sxs-lookup"><span data-stu-id="515af-130">From currency</span></span> | <span data-ttu-id="515af-131">До валюты</span><span class="sxs-lookup"><span data-stu-id="515af-131">To currency</span></span> | <span data-ttu-id="515af-132">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="515af-132">Start date</span></span> | <span data-ttu-id="515af-133">Курс обмена</span><span class="sxs-lookup"><span data-stu-id="515af-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="515af-134">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-134">EUR</span></span>           | <span data-ttu-id="515af-135">американский доллар</span><span class="sxs-lookup"><span data-stu-id="515af-135">USD</span></span>         | <span data-ttu-id="515af-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="515af-136">10/1/2015</span></span>  | <span data-ttu-id="515af-137">200</span><span class="sxs-lookup"><span data-stu-id="515af-137">200</span></span>           |
| <span data-ttu-id="515af-138">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-138">EUR</span></span>           | <span data-ttu-id="515af-139">американский доллар</span><span class="sxs-lookup"><span data-stu-id="515af-139">USD</span></span>         | <span data-ttu-id="515af-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="515af-140">11/1/2015</span></span>  | <span data-ttu-id="515af-141">150</span><span class="sxs-lookup"><span data-stu-id="515af-141">150</span></span>           |
| <span data-ttu-id="515af-142">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-142">EUR</span></span>           | <span data-ttu-id="515af-143">американский доллар</span><span class="sxs-lookup"><span data-stu-id="515af-143">USD</span></span>         | <span data-ttu-id="515af-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="515af-144">12/1/2012</span></span>  | <span data-ttu-id="515af-145">100</span><span class="sxs-lookup"><span data-stu-id="515af-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="515af-146">Выполните консолидацию на октябрь 2015</span><span class="sxs-lookup"><span data-stu-id="515af-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="515af-147">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="515af-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="515af-148">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="515af-148">Ledger account</span></span> | <span data-ttu-id="515af-149">Валютное</span><span class="sxs-lookup"><span data-stu-id="515af-149">Currency</span></span> | <span data-ttu-id="515af-150">Cумма</span><span class="sxs-lookup"><span data-stu-id="515af-150">Amount</span></span> | <span data-ttu-id="515af-151">Расчет</span><span class="sxs-lookup"><span data-stu-id="515af-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="515af-152">110110</span><span class="sxs-lookup"><span data-stu-id="515af-152">110110</span></span>         | <span data-ttu-id="515af-153">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-153">EUR</span></span>      | <span data-ttu-id="515af-154">250</span><span class="sxs-lookup"><span data-stu-id="515af-154">250</span></span>    | <span data-ttu-id="515af-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="515af-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="515af-156">130100</span><span class="sxs-lookup"><span data-stu-id="515af-156">130100</span></span>         | <span data-ttu-id="515af-157">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-157">EUR</span></span>      | <span data-ttu-id="515af-158">-250</span><span class="sxs-lookup"><span data-stu-id="515af-158">-250</span></span>   | <span data-ttu-id="515af-159">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="515af-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="515af-160">Выполните переоценку валюты для счета, начиная с 1-ого октября 2015 до 30-ого ноября 2015</span><span class="sxs-lookup"><span data-stu-id="515af-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="515af-161">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="515af-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="515af-162">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="515af-162">Ledger account</span></span> | <span data-ttu-id="515af-163">Валютное</span><span class="sxs-lookup"><span data-stu-id="515af-163">Currency</span></span> | <span data-ttu-id="515af-164">Cумма</span><span class="sxs-lookup"><span data-stu-id="515af-164">Amount</span></span>  | <span data-ttu-id="515af-165">Расчет</span><span class="sxs-lookup"><span data-stu-id="515af-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="515af-166">110110</span><span class="sxs-lookup"><span data-stu-id="515af-166">110110</span></span>         | <span data-ttu-id="515af-167">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-167">EUR</span></span>      | <span data-ttu-id="515af-168">333,33</span><span class="sxs-lookup"><span data-stu-id="515af-168">333.33</span></span>  | <span data-ttu-id="515af-169">Исходная сумма 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="515af-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="515af-170">130100</span><span class="sxs-lookup"><span data-stu-id="515af-170">130100</span></span>         | <span data-ttu-id="515af-171">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-171">EUR</span></span>      | <span data-ttu-id="515af-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="515af-172">-333.33</span></span> | <span data-ttu-id="515af-173">Исходная сумма -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="515af-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="515af-174">801400</span><span class="sxs-lookup"><span data-stu-id="515af-174">801400</span></span>         | <span data-ttu-id="515af-175">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-175">EUR</span></span>      | <span data-ttu-id="515af-176">83,33</span><span class="sxs-lookup"><span data-stu-id="515af-176">83.33</span></span>   | <span data-ttu-id="515af-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="515af-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="515af-178">801600</span><span class="sxs-lookup"><span data-stu-id="515af-178">801600</span></span>         | <span data-ttu-id="515af-179">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-179">EUR</span></span>      | <span data-ttu-id="515af-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="515af-180">-83.33</span></span>  | <span data-ttu-id="515af-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="515af-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="515af-182">Вы увидите дополнительные проводки для сумм в валюте отчетности.</span><span class="sxs-lookup"><span data-stu-id="515af-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="515af-183">Выполните переоценку валюты для счета, начиная с 1-ого октября 2015 до 31-ого декабря 2015</span><span class="sxs-lookup"><span data-stu-id="515af-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="515af-184">Сальдо в компании консолидации</span><span class="sxs-lookup"><span data-stu-id="515af-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="515af-185">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="515af-185">Ledger account</span></span> | <span data-ttu-id="515af-186">Валютное</span><span class="sxs-lookup"><span data-stu-id="515af-186">Currency</span></span> | <span data-ttu-id="515af-187">Cумма</span><span class="sxs-lookup"><span data-stu-id="515af-187">Amount</span></span>  | <span data-ttu-id="515af-188">Расчет</span><span class="sxs-lookup"><span data-stu-id="515af-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="515af-189">110110</span><span class="sxs-lookup"><span data-stu-id="515af-189">110110</span></span>         | <span data-ttu-id="515af-190">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-190">EUR</span></span>      | <span data-ttu-id="515af-191">500,00</span><span class="sxs-lookup"><span data-stu-id="515af-191">500.00</span></span>  | <span data-ttu-id="515af-192">Исходная сумма 500 × 1</span><span class="sxs-lookup"><span data-stu-id="515af-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="515af-193">130100</span><span class="sxs-lookup"><span data-stu-id="515af-193">130100</span></span>         | <span data-ttu-id="515af-194">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-194">EUR</span></span>      | <span data-ttu-id="515af-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="515af-195">-500.00</span></span> | <span data-ttu-id="515af-196">Исходная сумма -500 × 1</span><span class="sxs-lookup"><span data-stu-id="515af-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="515af-197">801400</span><span class="sxs-lookup"><span data-stu-id="515af-197">801400</span></span>         | <span data-ttu-id="515af-198">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-198">EUR</span></span>      | <span data-ttu-id="515af-199">250</span><span class="sxs-lookup"><span data-stu-id="515af-199">250</span></span>     | <span data-ttu-id="515af-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="515af-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="515af-201">801600</span><span class="sxs-lookup"><span data-stu-id="515af-201">801600</span></span>         | <span data-ttu-id="515af-202">Евро</span><span class="sxs-lookup"><span data-stu-id="515af-202">EUR</span></span>      | <span data-ttu-id="515af-203">-250</span><span class="sxs-lookup"><span data-stu-id="515af-203">-250</span></span>    | <span data-ttu-id="515af-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="515af-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






