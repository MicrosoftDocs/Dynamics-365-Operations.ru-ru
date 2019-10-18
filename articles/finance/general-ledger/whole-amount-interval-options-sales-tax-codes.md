---
title: Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов
description: В этой статье описываются параметры для поля "Метод расчета" в налоговых кодах, а также порядок расчета налога для интервалов и полных сумм.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb737e6600b1812c44d6101814fc858ac27013e9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185850"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="4974f-103">Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов</span><span class="sxs-lookup"><span data-stu-id="4974f-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="4974f-104">В этой статье описываются параметры для поля "Метод расчета" в налоговых кодах, а также порядок расчета налога для интервалов и полных сумм.</span><span class="sxs-lookup"><span data-stu-id="4974f-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="4974f-105">Вы можете настроить налоговый код для расчета на основе полной суммы или суммы в интервале.</span><span class="sxs-lookup"><span data-stu-id="4974f-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="4974f-106">Выберите способ расчета налогового кода на странице "Налоговые коды" с помощью поля "Метод расчета" на экспресс-вкладке "Расчет".</span><span class="sxs-lookup"><span data-stu-id="4974f-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="4974f-107">Полная сумма — ставка налога применяется ко всей налогооблагаемой сумме целиком.</span><span class="sxs-lookup"><span data-stu-id="4974f-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="4974f-108">Интервал — налогооблагаемая сумма делится на части, каждая из которых попадает в интервал, для которого установлена конкретная ставка налога.</span><span class="sxs-lookup"><span data-stu-id="4974f-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="4974f-109">Та часть суммы, которая попадает в указанный интервал, облагается налогом по ставке, установленной для данного интервала.</span><span class="sxs-lookup"><span data-stu-id="4974f-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="4974f-110">Налог представляет собой совокупность налоговых сумм, рассчитанных для каждого интервала сумм.</span><span class="sxs-lookup"><span data-stu-id="4974f-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="4974f-111">Параметр "Интервал" доступен только когда вы выбираете значение "Строка" в поле "Метод расчета" в области "Налог" на странице "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="4974f-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="4974f-112">Интервалы настраиваются на странице "Значения налогового кода" путем ввода минимальной и максимальной предельных сумм для каждой налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="4974f-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="4974f-113">Для того, чтобы налоги рассчитывались по всем налогооблагаемым суммам, вне зависимости от используемого метода должны соблюдаться следующие правила в отношении интервалов:</span><span class="sxs-lookup"><span data-stu-id="4974f-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="4974f-114">Минимальный предел первого интервала должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4974f-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="4974f-115">Максимальный предел последнего интервала должен быть равен нулю, который в данном случае обозначает бесконечность.</span><span class="sxs-lookup"><span data-stu-id="4974f-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="4974f-116">Максимальный предел интервала должен быть минимальным пределом следующего интервала.</span><span class="sxs-lookup"><span data-stu-id="4974f-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="4974f-117">Если сумма является максимальным пределом одного из интервалов и минимальным пределом следующего за ним интервала, то к этой сумме будет применена ставка налога, установленная для первого интервала.</span><span class="sxs-lookup"><span data-stu-id="4974f-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="4974f-118">Если сумма выходит за границы интервалов, которые определены верхним и нижним пределами, то применяется налоговая ставка равная 0.</span><span class="sxs-lookup"><span data-stu-id="4974f-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="4974f-119">Пример. Метод расчета "Сумма целиком"</span><span class="sxs-lookup"><span data-stu-id="4974f-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="4974f-120">На странице "Значения налогового кода" ставки налога устанавливаются в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="4974f-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4974f-121">**Нижний предел**</span><span class="sxs-lookup"><span data-stu-id="4974f-121">**Minimum limit**</span></span> | <span data-ttu-id="4974f-122">**Максимальный лимит**</span><span class="sxs-lookup"><span data-stu-id="4974f-122">**Maximum limit**</span></span> | <span data-ttu-id="4974f-123">**Ставка налога**</span><span class="sxs-lookup"><span data-stu-id="4974f-123">**Tax rate**</span></span> |
| <span data-ttu-id="4974f-124">0,00</span><span class="sxs-lookup"><span data-stu-id="4974f-124">0.00</span></span>              | <span data-ttu-id="4974f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-125">50.00</span></span>             | <span data-ttu-id="4974f-126">30%</span><span class="sxs-lookup"><span data-stu-id="4974f-126">30%</span></span>          |
| <span data-ttu-id="4974f-127">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-127">50.00</span></span>             | <span data-ttu-id="4974f-128">100,00</span><span class="sxs-lookup"><span data-stu-id="4974f-128">100.00</span></span>            | <span data-ttu-id="4974f-129">20%</span><span class="sxs-lookup"><span data-stu-id="4974f-129">20%</span></span>          |
| <span data-ttu-id="4974f-130">100,00</span><span class="sxs-lookup"><span data-stu-id="4974f-130">100.00</span></span>            | <span data-ttu-id="4974f-131">0,00</span><span class="sxs-lookup"><span data-stu-id="4974f-131">0.00</span></span>              | <span data-ttu-id="4974f-132">10%</span><span class="sxs-lookup"><span data-stu-id="4974f-132">10%</span></span>          |

<span data-ttu-id="4974f-133">Налог рассчитывается от всей налогооблагаемой суммы.</span><span class="sxs-lookup"><span data-stu-id="4974f-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="4974f-134">Налогооблагаемая сумма (цена)</span><span class="sxs-lookup"><span data-stu-id="4974f-134">Taxable amount (price)</span></span> | <span data-ttu-id="4974f-135">Расчет</span><span class="sxs-lookup"><span data-stu-id="4974f-135">Calculation</span></span>    | <span data-ttu-id="4974f-136">Налог (НСП)</span><span class="sxs-lookup"><span data-stu-id="4974f-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="4974f-137">35,00</span><span class="sxs-lookup"><span data-stu-id="4974f-137">35.00</span></span>                  | <span data-ttu-id="4974f-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4974f-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="4974f-139">10,50</span><span class="sxs-lookup"><span data-stu-id="4974f-139">10.50</span></span>     |
| <span data-ttu-id="4974f-140">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-140">50.00</span></span>                  | <span data-ttu-id="4974f-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4974f-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="4974f-142">15,00</span><span class="sxs-lookup"><span data-stu-id="4974f-142">15.00</span></span>     |
| <span data-ttu-id="4974f-143">85,00</span><span class="sxs-lookup"><span data-stu-id="4974f-143">85.00</span></span>                  | <span data-ttu-id="4974f-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="4974f-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="4974f-145">17,00</span><span class="sxs-lookup"><span data-stu-id="4974f-145">17.00</span></span>     |
| <span data-ttu-id="4974f-146">305,00</span><span class="sxs-lookup"><span data-stu-id="4974f-146">305.00</span></span>                 | <span data-ttu-id="4974f-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="4974f-147">305.00 \* 0.10</span></span> | <span data-ttu-id="4974f-148">30,50</span><span class="sxs-lookup"><span data-stu-id="4974f-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="4974f-149">Пример. Метод расчета "Интервал"</span><span class="sxs-lookup"><span data-stu-id="4974f-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="4974f-150">На странице "Значения" ставки налога устанавливаются в следующих интервалах.</span><span class="sxs-lookup"><span data-stu-id="4974f-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4974f-151">**Нижний предел**</span><span class="sxs-lookup"><span data-stu-id="4974f-151">**Minimum limit**</span></span> | <span data-ttu-id="4974f-152">**Максимальный лимит**</span><span class="sxs-lookup"><span data-stu-id="4974f-152">**Maximum limit**</span></span> | <span data-ttu-id="4974f-153">**Ставка налога**</span><span class="sxs-lookup"><span data-stu-id="4974f-153">**Tax rate**</span></span> |
| <span data-ttu-id="4974f-154">0,00</span><span class="sxs-lookup"><span data-stu-id="4974f-154">0.00</span></span>              | <span data-ttu-id="4974f-155">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-155">50.00</span></span>             | <span data-ttu-id="4974f-156">30%</span><span class="sxs-lookup"><span data-stu-id="4974f-156">30%</span></span>          |
| <span data-ttu-id="4974f-157">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-157">50.00</span></span>             | <span data-ttu-id="4974f-158">100,00</span><span class="sxs-lookup"><span data-stu-id="4974f-158">100.00</span></span>            | <span data-ttu-id="4974f-159">20%</span><span class="sxs-lookup"><span data-stu-id="4974f-159">20%</span></span>          |
| <span data-ttu-id="4974f-160">100,00</span><span class="sxs-lookup"><span data-stu-id="4974f-160">100.00</span></span>            | <span data-ttu-id="4974f-161">0,00</span><span class="sxs-lookup"><span data-stu-id="4974f-161">0.00</span></span>              | <span data-ttu-id="4974f-162">10%</span><span class="sxs-lookup"><span data-stu-id="4974f-162">10%</span></span>          |

<span data-ttu-id="4974f-163">Налог представляет собой совокупность налоговых сумм, рассчитанных для каждого интервала сумм.</span><span class="sxs-lookup"><span data-stu-id="4974f-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="4974f-164">Налогооблагаемая сумма (цена)</span><span class="sxs-lookup"><span data-stu-id="4974f-164">Taxable amount (price)</span></span> | <span data-ttu-id="4974f-165">Расчет</span><span class="sxs-lookup"><span data-stu-id="4974f-165">Calculation</span></span>                                                               | <span data-ttu-id="4974f-166">Налог (НСП)</span><span class="sxs-lookup"><span data-stu-id="4974f-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4974f-167">35,00</span><span class="sxs-lookup"><span data-stu-id="4974f-167">35.00</span></span>                  | <span data-ttu-id="4974f-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4974f-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4974f-169">10,50</span><span class="sxs-lookup"><span data-stu-id="4974f-169">10.50</span></span>     |
| <span data-ttu-id="4974f-170">50,00</span><span class="sxs-lookup"><span data-stu-id="4974f-170">50.00</span></span>                  | <span data-ttu-id="4974f-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4974f-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4974f-172">15,00</span><span class="sxs-lookup"><span data-stu-id="4974f-172">15.00</span></span>     |
| <span data-ttu-id="4974f-173">85,00</span><span class="sxs-lookup"><span data-stu-id="4974f-173">85.00</span></span>                  | <span data-ttu-id="4974f-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="4974f-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="4974f-175">22,00</span><span class="sxs-lookup"><span data-stu-id="4974f-175">22.00</span></span>     |
| <span data-ttu-id="4974f-176">305,00</span><span class="sxs-lookup"><span data-stu-id="4974f-176">305.00</span></span>                 | <span data-ttu-id="4974f-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="4974f-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="4974f-178">45,50</span><span class="sxs-lookup"><span data-stu-id="4974f-178">45.50</span></span>     |



<span data-ttu-id="4974f-179">Дополнительные сведения см. в разделе [Определение ставок налога на основе полей "База маржинальной прибыли" и "Метода расчета"](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="4974f-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





