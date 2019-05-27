---
title: Результаты амортизации со сторнированием
description: Эта статья описывает потенциальные последствия реверсирования проводки с основными средствами.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d624fa998329680d9fa471fa325f6fcfd3920c6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556303"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="2db4e-103">Результаты амортизации со сторнированием</span><span class="sxs-lookup"><span data-stu-id="2db4e-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db4e-104">Эта статья описывает потенциальные последствия реверсирования проводки с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="2db4e-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="2db4e-105">Имеется возможность реверсировать проводки по основным средствам, а также проводки, связанные с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="2db4e-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="2db4e-106">Кроме того, можно отменить реверсированную проводку.</span><span class="sxs-lookup"><span data-stu-id="2db4e-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="2db4e-107">Можно реверсировать или отменить реверсированную проводку, которая не является последней проводкой, разнесенной в книге для средства.</span><span class="sxs-lookup"><span data-stu-id="2db4e-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="2db4e-108">Сначала необходимо определить, разносились ли какие-либо проводки амортизации после той проводки, которая реверсируется.</span><span class="sxs-lookup"><span data-stu-id="2db4e-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="2db4e-109">Это необходимо, потому что амортизация не пересчитывается при реверсировании проводки.</span><span class="sxs-lookup"><span data-stu-id="2db4e-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="2db4e-110">Поэтому амортизация часто завышена или занижена после реверсирования, как показано в примерах.</span><span class="sxs-lookup"><span data-stu-id="2db4e-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="2db4e-111">Чтобы гарантировать правильность амортизации при реверсировании проводки, не продолжайте реверсирование в том случае, когда в процессе его выполнения получено сообщение, информирующее о том, что амортизация не будет пересчитана.</span><span class="sxs-lookup"><span data-stu-id="2db4e-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="2db4e-112">Вместо этого сначала отмените проводку по амортизации, которая была разнесена после той проводки, которую вы пытаетесь реверсировать, а затем продолжите реверсирование.</span><span class="sxs-lookup"><span data-stu-id="2db4e-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="2db4e-113">Теперь сообщение о невозможности пересчета амортизации не появится, и можно будет выполнить реверсирование.</span><span class="sxs-lookup"><span data-stu-id="2db4e-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="2db4e-114">Следующие примеры иллюстрируют вычисления, которые будут произведены в том случае, если проигнорировать предупреждающее сообщение и продолжить реверсирование проводки без предварительной отмены проводок по амортизации.</span><span class="sxs-lookup"><span data-stu-id="2db4e-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="2db4e-115">Пример 1: Амортизация завышена</span><span class="sxs-lookup"><span data-stu-id="2db4e-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="2db4e-116">Настройка средства подразумевает 5-летний срок жизни и линейную амортизацию (60 периодов амортизации).</span><span class="sxs-lookup"><span data-stu-id="2db4e-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="2db4e-117">В этом примере амортизация завышена.</span><span class="sxs-lookup"><span data-stu-id="2db4e-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="2db4e-118">Журнал проводок активов</span><span class="sxs-lookup"><span data-stu-id="2db4e-118">Asset transaction history</span></span>

| <span data-ttu-id="2db4e-119">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-119">Date</span></span>       | <span data-ttu-id="2db4e-120">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-120">Transaction type</span></span>                                                          | <span data-ttu-id="2db4e-121">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2db4e-122">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-122">January 1</span></span>  | <span data-ttu-id="2db4e-123">Ввод в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="2db4e-123">Acquisition</span></span>                                                               | <span data-ttu-id="2db4e-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-124">59,000.00</span></span>                                 |
| <span data-ttu-id="2db4e-125">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-125">January 1</span></span>  | <span data-ttu-id="2db4e-126">Переоценка стоимости ввода в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="2db4e-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="2db4e-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-127">1,000.00</span></span>                                  |
| <span data-ttu-id="2db4e-128">31 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-128">January 31</span></span> | <span data-ttu-id="2db4e-129">Амортизация (создано с помощью предложения для одного периода амортизации)</span><span class="sxs-lookup"><span data-stu-id="2db4e-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="2db4e-130">1000,00 Расчет: остаточная стоимость (59000 + 1000) / Число оставшихся периодов амортизации (60)</span><span class="sxs-lookup"><span data-stu-id="2db4e-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="2db4e-131">Действие реверсирования</span><span class="sxs-lookup"><span data-stu-id="2db4e-131">Reversal action</span></span>

| <span data-ttu-id="2db4e-132">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-132">Date</span></span>      | <span data-ttu-id="2db4e-133">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-133">Transaction type</span></span>                | <span data-ttu-id="2db4e-134">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="2db4e-135">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-135">January 1</span></span> | <span data-ttu-id="2db4e-136">Сторнирование переоценки стоимости ввода в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="2db4e-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="2db4e-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="2db4e-138">Влияние амортизации</span><span class="sxs-lookup"><span data-stu-id="2db4e-138">Depreciation effect</span></span>

| <span data-ttu-id="2db4e-139">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-139">Date</span></span>        | <span data-ttu-id="2db4e-140">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-140">Transaction type</span></span>        | <span data-ttu-id="2db4e-141">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2db4e-142">28 февраля</span><span class="sxs-lookup"><span data-stu-id="2db4e-142">February 28</span></span> | <span data-ttu-id="2db4e-143">Амортизация (предложение)</span><span class="sxs-lookup"><span data-stu-id="2db4e-143">Depreciation (proposal)</span></span> | <span data-ttu-id="2db4e-144">983,05 Расчет: остаточная стоимость (59000 – 1000 амортизация) / Число оставшихся периодов амортизации (59)</span><span class="sxs-lookup"><span data-stu-id="2db4e-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="2db4e-145">Амортизация завышена на 16,95 (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="2db4e-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="2db4e-146">Пример 2: Амортизация занижена</span><span class="sxs-lookup"><span data-stu-id="2db4e-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="2db4e-147">Настройка средства подразумевает 5-летний срок жизни и линейную амортизацию (60 периодов амортизации).</span><span class="sxs-lookup"><span data-stu-id="2db4e-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="2db4e-148">В этом примере амортизация занижена.</span><span class="sxs-lookup"><span data-stu-id="2db4e-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="2db4e-149">Журнал проводок активов</span><span class="sxs-lookup"><span data-stu-id="2db4e-149">Asset transaction history</span></span>

| <span data-ttu-id="2db4e-150">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-150">Date</span></span>       | <span data-ttu-id="2db4e-151">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-151">Transaction type</span></span>                                                          | <span data-ttu-id="2db4e-152">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="2db4e-153">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-153">January 1</span></span>  | <span data-ttu-id="2db4e-154">Приобретение</span><span class="sxs-lookup"><span data-stu-id="2db4e-154">Acquisition</span></span>                                                               | <span data-ttu-id="2db4e-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-155">59,000.00</span></span>                                   |
| <span data-ttu-id="2db4e-156">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-156">January 1</span></span>  | <span data-ttu-id="2db4e-157">Корректировка уценки</span><span class="sxs-lookup"><span data-stu-id="2db4e-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="2db4e-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-158">1,000.00</span></span>                                    |
| <span data-ttu-id="2db4e-159">31 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-159">January 31</span></span> | <span data-ttu-id="2db4e-160">Амортизация (создано с помощью предложения для одного периода амортизации)</span><span class="sxs-lookup"><span data-stu-id="2db4e-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="2db4e-161">966,67 Расчет: остаточная стоимость (59000 + 1000) / Число оставшихся периодов амортизации (60)</span><span class="sxs-lookup"><span data-stu-id="2db4e-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="2db4e-162">Действие реверсирования</span><span class="sxs-lookup"><span data-stu-id="2db4e-162">Reversal action</span></span>

| <span data-ttu-id="2db4e-163">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-163">Date</span></span>      | <span data-ttu-id="2db4e-164">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-164">Transaction type</span></span>               | <span data-ttu-id="2db4e-165">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="2db4e-166">1 января</span><span class="sxs-lookup"><span data-stu-id="2db4e-166">January 1</span></span> | <span data-ttu-id="2db4e-167">Реверсирование корректировки уценки</span><span class="sxs-lookup"><span data-stu-id="2db4e-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="2db4e-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="2db4e-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="2db4e-169">Влияние амортизации</span><span class="sxs-lookup"><span data-stu-id="2db4e-169">Depreciation effect</span></span>

| <span data-ttu-id="2db4e-170">Дата</span><span class="sxs-lookup"><span data-stu-id="2db4e-170">Date</span></span>        | <span data-ttu-id="2db4e-171">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="2db4e-171">Transaction type</span></span>        | <span data-ttu-id="2db4e-172">Сумма</span><span class="sxs-lookup"><span data-stu-id="2db4e-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db4e-173">28 февраля</span><span class="sxs-lookup"><span data-stu-id="2db4e-173">February 28</span></span> | <span data-ttu-id="2db4e-174">Амортизация (предложение)</span><span class="sxs-lookup"><span data-stu-id="2db4e-174">Depreciation (proposal)</span></span> | <span data-ttu-id="2db4e-175">983,62 Расчет: остаточная стоимость (59000 – 1000 амортизация) / Число оставшихся периодов амортизации (59)</span><span class="sxs-lookup"><span data-stu-id="2db4e-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="2db4e-176">Амортизация занижена на 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="2db4e-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="2db4e-177">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2db4e-177">Additional resources</span></span>
--------

[<span data-ttu-id="2db4e-178">Амортизация ОС</span><span class="sxs-lookup"><span data-stu-id="2db4e-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



