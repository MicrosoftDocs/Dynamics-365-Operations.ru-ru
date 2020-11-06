---
title: Налоговые платежи и правила округления
description: Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998dbd01352d3fa5040187e81b564d14133464db
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014967"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="fbdc9-103">Налоговые платежи и правила округления</span><span class="sxs-lookup"><span data-stu-id="fbdc9-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbdc9-104">Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="fbdc9-105">Периодически необходимо сдавать отчеты и уплачивать налоги налоговым ведомствам.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="fbdc9-106">Это может быть сделано путем выполнения процесса сопоставления и разноски налогов на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="fbdc9-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="fbdc9-107">Налог за период будет сопоставлен налоговым счетам, и сальдо налога будет разнесено на счет сопоставления налога.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="fbdc9-108">Сальдо налога, которое разнесено на счет сопоставления налога, может округляться согласно требованиям налоговых ведомств путем настройки правила округления на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="fbdc9-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="fbdc9-109">Разница округления разносится на счет округления налога, который выбирается в поле "Счета для автоматических проводок" в главной книге.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="fbdc9-110">Приведенный ниже пример иллюстрирует работу правила округления для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="fbdc9-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="fbdc9-111">Examples</span></span>

<span data-ttu-id="fbdc9-112">Полный налог на продажу за период показывает кредитовое сальдо -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="fbdc9-113">Юридическое лицо собрало больше налога, чем уплатило.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="fbdc9-114">Поэтому у юридического лица имеется денежное обязательство перед налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="fbdc9-115">Юридическому лицу необходимо использовать метод округления сальдо до ближайшей кратной 1,00 суммы.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="fbdc9-116">Пользователь, ответственный за учет налогов, должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="fbdc9-117">Нажмите **Налог** > **Косвенные налоги** > **Налог** > **Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="fbdc9-118">На экспресс-вкладке **Общие** в поле **Способ округления** выберите значение **Обычный**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="fbdc9-119">В поле **Округление** введите 1,00.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="fbdc9-120">Когда наступит срок уплаты налогов налоговому органу, выберите **Налог** > **Декларации** > **Налог** > **Сопоставить и разнести налог**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="fbdc9-121">В счете сопоставления налога можно видеть, что сумма налогового обязательства **98 765,43** округляется до **98 765**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="fbdc9-122">В следующей таблице показано, как сумма 98 765,43 округляется с использованием каждого из методов округления, доступных в поле **Способ округления** на странице **Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="fbdc9-123">Если значение округления устанавливается как 0,00, то:</span><span class="sxs-lookup"><span data-stu-id="fbdc9-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="fbdc9-124">Для обычного округления поведение округления такое же, как в случае **Округление = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="fbdc9-125">Для параметров **Способ округления** **Вниз** , **Округление вверх** и **Собственное преимущество** поведение при округлении такое же, как в случае **Округление = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-125">For the **Rounding form options** , **Downward** , **Rounding-up** , and **Own advantage** , the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="fbdc9-126">Параметр способа округления</span><span class="sxs-lookup"><span data-stu-id="fbdc9-126">Rounding form option</span></span>                | <span data-ttu-id="fbdc9-127">Значение округления = 0,01</span><span class="sxs-lookup"><span data-stu-id="fbdc9-127">Round-off value = 0.01</span></span> | <span data-ttu-id="fbdc9-128">Значение округления = 0,10</span><span class="sxs-lookup"><span data-stu-id="fbdc9-128">Round-off value = 0.10</span></span> | <span data-ttu-id="fbdc9-129">Значение округления = 1,00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-129">Round-off value = 1.00</span></span> | <span data-ttu-id="fbdc9-130">Значение округления = 100,00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-130">Round-off value = 100.00</span></span> | <span data-ttu-id="fbdc9-131">Значение округления = 0,00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="fbdc9-132">Обычный</span><span class="sxs-lookup"><span data-stu-id="fbdc9-132">Normal</span></span>                              | <span data-ttu-id="fbdc9-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-133">98,765.43</span></span>              | <span data-ttu-id="fbdc9-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="fbdc9-134">98,765.40</span></span>              | <span data-ttu-id="fbdc9-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-135">98,765.00</span></span>              | <span data-ttu-id="fbdc9-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-136">98,800.00</span></span>                | <span data-ttu-id="fbdc9-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-137">98,765.43</span></span>                |
| <span data-ttu-id="fbdc9-138">В меньшую сторону</span><span class="sxs-lookup"><span data-stu-id="fbdc9-138">Downward</span></span>                            | <span data-ttu-id="fbdc9-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-139">98,765.43</span></span>              | <span data-ttu-id="fbdc9-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="fbdc9-140">98,765.40</span></span>              | <span data-ttu-id="fbdc9-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-141">98,765.00</span></span>              | <span data-ttu-id="fbdc9-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-142">98,700.00</span></span>                | <span data-ttu-id="fbdc9-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-143">98,765.00</span></span>                |
| <span data-ttu-id="fbdc9-144">В большую сторону</span><span class="sxs-lookup"><span data-stu-id="fbdc9-144">Rounding-up</span></span>                         | <span data-ttu-id="fbdc9-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-145">98,765.43</span></span>              | <span data-ttu-id="fbdc9-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="fbdc9-146">98,765.50</span></span>              | <span data-ttu-id="fbdc9-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-147">98,766.00</span></span>              | <span data-ttu-id="fbdc9-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-148">98,800.00</span></span>                | <span data-ttu-id="fbdc9-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-149">98,766.00</span></span>                |
| <span data-ttu-id="fbdc9-150">Собственное преимущество, для кредитового сальдо</span><span class="sxs-lookup"><span data-stu-id="fbdc9-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="fbdc9-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-151">98,765.43</span></span>              | <span data-ttu-id="fbdc9-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="fbdc9-152">98,765.40</span></span>              | <span data-ttu-id="fbdc9-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-153">98,765.00</span></span>              | <span data-ttu-id="fbdc9-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-154">98,700.00</span></span>                | <span data-ttu-id="fbdc9-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-155">98,765.00</span></span>                |
| <span data-ttu-id="fbdc9-156">Собственное преимущество, для дебетового сальдо</span><span class="sxs-lookup"><span data-stu-id="fbdc9-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="fbdc9-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="fbdc9-157">98,765.43</span></span>              | <span data-ttu-id="fbdc9-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="fbdc9-158">98,765.50</span></span>              | <span data-ttu-id="fbdc9-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-159">98,766.00</span></span>              | <span data-ttu-id="fbdc9-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-160">98,800.00</span></span>                | <span data-ttu-id="fbdc9-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="fbdc9-162">Обычное округление, и точность округления равна 0,01</span><span class="sxs-lookup"><span data-stu-id="fbdc9-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="fbdc9-163">Округление</span><span class="sxs-lookup"><span data-stu-id="fbdc9-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="fbdc9-164">Процесс расчета</span><span class="sxs-lookup"><span data-stu-id="fbdc9-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="fbdc9-165">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="fbdc9-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="fbdc9-166">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="fbdc9-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="fbdc9-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="fbdc9-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="fbdc9-168">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="fbdc9-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="fbdc9-169">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="fbdc9-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="fbdc9-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="fbdc9-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="fbdc9-171">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="fbdc9-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="fbdc9-172">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="fbdc9-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="fbdc9-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="fbdc9-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="fbdc9-174">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="fbdc9-175">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="fbdc9-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="fbdc9-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="fbdc9-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="fbdc9-177">При выборе "Собственное преимущество" округление всегда производится в пользу юридического лица.</span><span class="sxs-lookup"><span data-stu-id="fbdc9-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="fbdc9-178">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="fbdc9-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="fbdc9-179">Обзор налога</span><span class="sxs-lookup"><span data-stu-id="fbdc9-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="fbdc9-180">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="fbdc9-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="fbdc9-181">Создание налоговых проводок по документам</span><span class="sxs-lookup"><span data-stu-id="fbdc9-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="fbdc9-182">Просмотр разнесенных налоговых проводок</span><span class="sxs-lookup"><span data-stu-id="fbdc9-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="fbdc9-183">Функция round</span><span class="sxs-lookup"><span data-stu-id="fbdc9-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


