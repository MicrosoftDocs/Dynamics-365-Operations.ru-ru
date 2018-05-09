---
title: "Ставки налога на основе базы маржинальной прибыли и методов расчета"
description: "В этом разделе описываются, как значения в полях \"База маржинальной прибыли\" и \"Метод расчета\" определяют ставку налога в проводках продажи и покупки."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9bd67a2c7eed658b27b208bdb428bb880708cd31
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="16ede-103">Ставки налога на основе базы маржинальной прибыли и методов расчета</span><span class="sxs-lookup"><span data-stu-id="16ede-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16ede-104">В этом разделе описываются, как значения в полях "База маржинальной прибыли" и "Метод расчета" определяют ставку налога в проводках продажи и покупки.</span><span class="sxs-lookup"><span data-stu-id="16ede-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="16ede-105">База маржинальной прибыли на экспресс-вкладке "Расчет" на странице "Налоговые коды" определяет количество, которое используется для комплектации соответствующей налоговой ставки (ставок) по ставкам на странице значений налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="16ede-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="16ede-106">Тип количества в поле базы маржинальной прибыли в сочетании с методом в поле метода расчета определяет логику поиска правильной налоговой ставки (ставок) для транзакции.</span><span class="sxs-lookup"><span data-stu-id="16ede-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="16ede-107">Различные комбинации значений в этих полях дают в результате сильно отличающиеся друг от друга расчеты налога, как показано на следующих примерах</span><span class="sxs-lookup"><span data-stu-id="16ede-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="16ede-108">В этих примерах используются одинаковые значения налогового интервала, которые настроены для каждого налогового кода на странице "Значения налоговых кодов".</span><span class="sxs-lookup"><span data-stu-id="16ede-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="16ede-109">Чтобы открыть эту страницу, щелкните "Налоговый код" &gt; значения на странице налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="16ede-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="16ede-110">Если база маржинальной прибыли по одному или нескольким налоговым кодам основана на сумме строк или единиц, то значение в поле "Метод расчета" на странице "параметры ГК" должно быть задано как "Строка".</span><span class="sxs-lookup"><span data-stu-id="16ede-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="16ede-111">Чистая сумма по строке</span><span class="sxs-lookup"><span data-stu-id="16ede-111">Net amount per line</span></span>
<span data-ttu-id="16ede-112">Выберите этот параметр для определения ставок налога на основе чистой суммы по строкам накладной, исключая все прочие налоги.</span><span class="sxs-lookup"><span data-stu-id="16ede-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="16ede-113">пример</span><span class="sxs-lookup"><span data-stu-id="16ede-113">Example</span></span>

<span data-ttu-id="16ede-114">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-115">Интервал суммы</span><span class="sxs-lookup"><span data-stu-id="16ede-115">Amount interval</span></span>    | <span data-ttu-id="16ede-116">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="16ede-117">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-117">0 - 50</span></span>             | <span data-ttu-id="16ede-118">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-118">30%</span></span>      |
| <span data-ttu-id="16ede-119">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-119">50 - 100</span></span>           | <span data-ttu-id="16ede-120">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-120">20%</span></span>      |
| <span data-ttu-id="16ede-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-122">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="16ede-123">Верхняя граница последнего интервала равная 0 означает, что все суммы больше 100 включаются в этот интервал.</span><span class="sxs-lookup"><span data-stu-id="16ede-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="16ede-124">База маржинальной прибыли: **Чистая сумма по строке**</span><span class="sxs-lookup"><span data-stu-id="16ede-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="16ede-125">Метод расчета: **Интервал**</span><span class="sxs-lookup"><span data-stu-id="16ede-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="16ede-126">Приобретается 8 ламп по цене 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="16ede-127">Чистая сумма для этой строки накладной равна 200 евро.</span><span class="sxs-lookup"><span data-stu-id="16ede-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="16ede-128">Налог вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16ede-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="16ede-129">Итоговая сумма налога = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="16ede-130">Итоговая сумма накладной = 200,00 + 35,00 = 235,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="16ede-131">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="16ede-131">**Variation**</span></span> 

<span data-ttu-id="16ede-132">Если накладная содержит две строки, каждая из которых включает четыре номенклатуры, чистая сумма по каждой строке равна 100,00, и налог вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16ede-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="16ede-133">Налог по строке 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="16ede-134">Налог по строке 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="16ede-135">Итого налог = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="16ede-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="16ede-136">Итоговая сумма накладной = 200,00 + 50,00 = 250,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="16ede-137">Чистая сумма на единицу</span><span class="sxs-lookup"><span data-stu-id="16ede-137">Net amount per unit</span></span>
<span data-ttu-id="16ede-138">Выберите этот параметр для определения ставок налога на основе стоимости каждой единицы измерения, исключая все прочие налоги.</span><span class="sxs-lookup"><span data-stu-id="16ede-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="16ede-139">Когда выбрана единица, основанная на базе маржинальной прибыли, также необходимо указать единицу для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="16ede-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="16ede-140">Пример</span><span class="sxs-lookup"><span data-stu-id="16ede-140">Example</span></span>

<span data-ttu-id="16ede-141">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-142">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="16ede-142">Amount</span></span>             | <span data-ttu-id="16ede-143">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="16ede-144">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-144">0 - 50</span></span>             | <span data-ttu-id="16ede-145">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-145">30%</span></span>      |
| <span data-ttu-id="16ede-146">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-146">50 - 100</span></span>           | <span data-ttu-id="16ede-147">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-147">20%</span></span>      |
| <span data-ttu-id="16ede-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-149">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-149">10%</span></span>      |

<span data-ttu-id="16ede-150">База маржинальной прибыли: **Чистая сумма на единицу**</span><span class="sxs-lookup"><span data-stu-id="16ede-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="16ede-151">Метод расчета: **Сумма целиком**</span><span class="sxs-lookup"><span data-stu-id="16ede-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="16ede-152">Приобретается 8 ламп по цене 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="16ede-153">Чистая сумма для этой строки накладной равна 200 евро.</span><span class="sxs-lookup"><span data-stu-id="16ede-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="16ede-154">Налог высчитан следующим образом: налог на единицу измерения = 25,00 x 30% = 7,50 Итоговая сумма налога = 7,50 x 8 единиц = 60,00 Итоговая сумма накладной = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="16ede-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="16ede-155">Чистая сумма сальдо по накладной</span><span class="sxs-lookup"><span data-stu-id="16ede-155">Net amount of invoice balance</span></span>

<span data-ttu-id="16ede-156">Выберите этот параметр для определения ставок налога на основе общей суммы по накладной, исключая все прочие налоги.</span><span class="sxs-lookup"><span data-stu-id="16ede-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="16ede-157">пример</span><span class="sxs-lookup"><span data-stu-id="16ede-157">Example</span></span>

<span data-ttu-id="16ede-158">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-159">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="16ede-159">Amount</span></span>            | <span data-ttu-id="16ede-160">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="16ede-161">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-161">0 - 50</span></span>            | <span data-ttu-id="16ede-162">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-162">30%</span></span>      |
| <span data-ttu-id="16ede-163">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-163">50 - 100</span></span>          | <span data-ttu-id="16ede-164">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-164">20%</span></span>      |
| <span data-ttu-id="16ede-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-166">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-166">10%</span></span>      |

<span data-ttu-id="16ede-167">База маржинальной прибыли: **Чистая сумма сальдо по накладной**</span><span class="sxs-lookup"><span data-stu-id="16ede-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="16ede-168">Метод расчета: **Интервал** В накладной по продаже есть 2 строки с 4 лампами в каждой строке по 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="16ede-169">Чистая сумма сальдо по накладной — 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="16ede-170">Налог высчитан следующим образом: итоговая сумма налога = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Итоговая сумма накладной = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="16ede-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="16ede-171">Валовая сумма по строке</span><span class="sxs-lookup"><span data-stu-id="16ede-171">Gross amount per line</span></span>

<span data-ttu-id="16ede-172">Выберите этот параметр для определения ставок налога на основе значения строки, включающее все прочие налоги для этой строки.</span><span class="sxs-lookup"><span data-stu-id="16ede-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="16ede-173">В налоговой группе может быть только один налоговый код, для которого в поле "База маржинальной прибыли" выбран этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16ede-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="16ede-174">Пример</span><span class="sxs-lookup"><span data-stu-id="16ede-174">Example</span></span>

<span data-ttu-id="16ede-175">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-176">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="16ede-176">Amount</span></span>             | <span data-ttu-id="16ede-177">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="16ede-178">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-178">0 - 50</span></span>             | <span data-ttu-id="16ede-179">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-179">30%</span></span>      |
| <span data-ttu-id="16ede-180">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-180">50 - 100</span></span>           | <span data-ttu-id="16ede-181">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-181">20%</span></span>      |
| <span data-ttu-id="16ede-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-183">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-183">10%</span></span>      |

<span data-ttu-id="16ede-184">База маржинальной прибыли: **Валовая сумма по строке** Метод расчета: **Интервал** Дополнительно есть другой налоговый код, вычисленный для специальной пошлины 5,00 по каждой лампе.</span><span class="sxs-lookup"><span data-stu-id="16ede-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="16ede-185">Пошлина добавляется к чистой сумме до расчета налога.</span><span class="sxs-lookup"><span data-stu-id="16ede-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="16ede-186">Приобретается 8 ламп по цене 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="16ede-187">Чистая сумма для этой строки накладной равна 200 евро.</span><span class="sxs-lookup"><span data-stu-id="16ede-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="16ede-188">Валовая сумма для этой строки накладной равна 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="16ede-189">Налог вычисляется следующим образом: итоговая сумма налога = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Итоговая пошлина = 5,00 x 8 = 40,00 Итоговая сумма накладной = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="16ede-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="16ede-190">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="16ede-190">**Variation**</span></span> 

<span data-ttu-id="16ede-191">Если накладная создается с использованием 2 строк, каждая из которых включает 4 номенклатуры, чистая сумма по каждой строке накладной равна 100,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="16ede-192">Валовая сумма (включая пошлину 4 x 5,00) по стирке накладной будет 120,00, и налог создается следующим образом: сумма налога по строке накладной 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 сумма налога по строке накладной 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Итоговая сумма налога = 27,00 + 27,00 = 54,00 Итоговая пошлина = 5,00 x 8 = 40,00 Общая сумма накладной = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="16ede-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="16ede-193">Валовая сумма на единицу</span><span class="sxs-lookup"><span data-stu-id="16ede-193">Gross amount per unit</span></span>

<span data-ttu-id="16ede-194">Выберите этот параметр для определения ставок налога на основе стоимости единицы измерения, включая все прочие налоги.</span><span class="sxs-lookup"><span data-stu-id="16ede-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="16ede-195">В налоговой группе может быть только один налоговый код, для которого в поле "База маржинальной прибыли" выбран этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16ede-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="16ede-196">Пример</span><span class="sxs-lookup"><span data-stu-id="16ede-196">Example</span></span>

<span data-ttu-id="16ede-197">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-198">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="16ede-198">Amount</span></span>             | <span data-ttu-id="16ede-199">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="16ede-200">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-200">0 - 50</span></span>             | <span data-ttu-id="16ede-201">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-201">30%</span></span>      |
| <span data-ttu-id="16ede-202">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-202">50 - 100</span></span>           | <span data-ttu-id="16ede-203">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-203">20%</span></span>      |
| <span data-ttu-id="16ede-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-205">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-205">10%</span></span>      |

<span data-ttu-id="16ede-206">База маржинальной прибыли: **Валовая сумма на единицу** Уплачивается особая пошлина в сумме 5,00 на каждую лампу.</span><span class="sxs-lookup"><span data-stu-id="16ede-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="16ede-207">Пошлина добавляется к чистой сумме до расчета налога.</span><span class="sxs-lookup"><span data-stu-id="16ede-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="16ede-208">Приобретается 8 ламп по цене 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="16ede-209">Валовая сумма на единицу измерения равна 30,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="16ede-210">Налог высчитан следующим образом: налог на единицу измерения = 30 x 30% = 9,00 Итоговая сумма налога = 9,00 x 8 = 72,00 Итоговая пошлина = 5,00 x 8 = 40,00 Итоговая сумма накладной = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="16ede-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="16ede-211">Общая сумма накладной, включая все прочие налоги</span><span class="sxs-lookup"><span data-stu-id="16ede-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="16ede-212">Выберите этот параметр для определения ставок налога на основе общей суммы по накладной, включая все прочие налоги.</span><span class="sxs-lookup"><span data-stu-id="16ede-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="16ede-213">В налоговой группе может быть только один налоговый код, для которого в поле "База маржинальной прибыли" выбран этот параметр</span><span class="sxs-lookup"><span data-stu-id="16ede-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="16ede-214">Пример</span><span class="sxs-lookup"><span data-stu-id="16ede-214">Example</span></span>

<span data-ttu-id="16ede-215">Настройка ставок налога выполнена в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="16ede-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="16ede-216">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="16ede-216">Amount</span></span>             | <span data-ttu-id="16ede-217">Ставка налога</span><span class="sxs-lookup"><span data-stu-id="16ede-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="16ede-218">0-50</span><span class="sxs-lookup"><span data-stu-id="16ede-218">0 - 50</span></span>             | <span data-ttu-id="16ede-219">30%</span><span class="sxs-lookup"><span data-stu-id="16ede-219">30%</span></span>      |
| <span data-ttu-id="16ede-220">50-100</span><span class="sxs-lookup"><span data-stu-id="16ede-220">50 - 100</span></span>           | <span data-ttu-id="16ede-221">20%</span><span class="sxs-lookup"><span data-stu-id="16ede-221">20%</span></span>      |
| <span data-ttu-id="16ede-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="16ede-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="16ede-223">10%</span><span class="sxs-lookup"><span data-stu-id="16ede-223">10%</span></span>      |

<span data-ttu-id="16ede-224">База маржинальной прибыли: **Общая сумма накладной, включая все прочие налоги** Метода расчета: **Интервал** </span><span class="sxs-lookup"><span data-stu-id="16ede-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="16ede-225">Уплачивается особая пошлина в сумме 5,00 на каждую лампу.</span><span class="sxs-lookup"><span data-stu-id="16ede-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="16ede-226">Пошлина добавляется к чистой сумме до расчета налога.</span><span class="sxs-lookup"><span data-stu-id="16ede-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="16ede-227">Приобретается 8 ламп по цене 25,00 каждая.</span><span class="sxs-lookup"><span data-stu-id="16ede-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="16ede-228">Чистая сумма накладной составляет 200,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="16ede-229">Валовая сумма накладной равна 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="16ede-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="16ede-230">Налог вычисляется следующим образом: итоговая сумма налога = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Итоговая пошлина = 5,00 x 8 = 40,00 Итоговая сумма накладной = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="16ede-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="16ede-231">Дополнительные сведения см. в разделах [Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов](whole-amount-interval-options-sales-tax-codes.md) и [Методы расчета налога в поле "Основание"](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="16ede-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>




