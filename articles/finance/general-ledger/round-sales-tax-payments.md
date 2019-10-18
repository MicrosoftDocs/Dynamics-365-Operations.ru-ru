---
title: Налоговые платежи и правила округления
description: Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
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
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186333"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="6d6f8-103">Налоговые платежи и правила округления</span><span class="sxs-lookup"><span data-stu-id="6d6f8-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d6f8-104">Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="6d6f8-105">Периодически необходимо сдавать отчеты и уплачивать налоги налоговым ведомствам.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="6d6f8-106">Это может быть сделано путем выполнения процесса сопоставления и разноски налогов на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="6d6f8-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="6d6f8-107">Налог за период будет сопоставлен налоговым счетам, и сальдо налога будет разнесено на счет сопоставления налога.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="6d6f8-108">Сальдо налога, которое разнесено на счет сопоставления налога, может округляться согласно требованиям налоговых ведомств путем настройки правила округления на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="6d6f8-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="6d6f8-109">Разница округления разносится на счет округления налога, который выбирается в поле "Счета для автоматических проводок" в главной книге.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="6d6f8-110">Приведенный ниже пример иллюстрирует работу правила округления для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="6d6f8-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d6f8-111">Examples</span></span>

<span data-ttu-id="6d6f8-112">Полный налог на продажу за период показывает кредитовое сальдо -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="6d6f8-113">Юридическое лицо собрало больше налога, чем уплатило.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="6d6f8-114">Поэтому у юридического лица имеется денежное обязательство перед налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="6d6f8-115">Юридическому лицу необходимо использовать метод округления сальдо до ближайшей кратной 1,00 суммы.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="6d6f8-116">Пользователь, ответственный за учет налогов, должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="6d6f8-117">Нажмите "Налог" &gt; "Косвенные налоги" &gt; "Налог" &gt; "Налоговые органы"</span><span class="sxs-lookup"><span data-stu-id="6d6f8-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="6d6f8-118">На экспресс-вкладке "Общие" выберите значение "Обычный" в поле "Способ округления".</span><span class="sxs-lookup"><span data-stu-id="6d6f8-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="6d6f8-119">В поле "Округление" введите 1,00.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="6d6f8-120">Когда наступит срок уплаты налогов налоговому органу, откройте страницу "Сопоставить и разнести налог".</span><span class="sxs-lookup"><span data-stu-id="6d6f8-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="6d6f8-121">(Нажмите "Налог" &gt; "Объявления" &gt; "Налог" &gt; "Сопоставить и разнести налог".)</span><span class="sxs-lookup"><span data-stu-id="6d6f8-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="6d6f8-122">В счете сопоставления налога сумма налогового обязательства 98 765,43 округляется до 98 765.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="6d6f8-123">В следующей таблице показано, как сумма 98 765,43 округляется с использованием каждого из методов округления, доступных в поле "Способ округления" на странице "Налоговые органы".</span><span class="sxs-lookup"><span data-stu-id="6d6f8-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="6d6f8-124">Параметр способа округления</span><span class="sxs-lookup"><span data-stu-id="6d6f8-124">Rounding form option</span></span>                | <span data-ttu-id="6d6f8-125">Значение округления = 0,01</span><span class="sxs-lookup"><span data-stu-id="6d6f8-125">Round-off value = 0.01</span></span> | <span data-ttu-id="6d6f8-126">Значение округления = 0,10</span><span class="sxs-lookup"><span data-stu-id="6d6f8-126">Round-off value = 0.10</span></span> | <span data-ttu-id="6d6f8-127">Значение округления = 1,00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-127">Round-off value = 1.00</span></span> | <span data-ttu-id="6d6f8-128">Значение округления = 100,00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="6d6f8-129">Обычная</span><span class="sxs-lookup"><span data-stu-id="6d6f8-129">Normal</span></span>                              | <span data-ttu-id="6d6f8-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6d6f8-130">98,765.43</span></span>              | <span data-ttu-id="6d6f8-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6d6f8-131">98,765.40</span></span>              | <span data-ttu-id="6d6f8-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-132">98,765.00</span></span>              | <span data-ttu-id="6d6f8-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-133">98,800.00</span></span>                |
| <span data-ttu-id="6d6f8-134">В меньшую сторону</span><span class="sxs-lookup"><span data-stu-id="6d6f8-134">Downward</span></span>                            | <span data-ttu-id="6d6f8-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6d6f8-135">98,765.43</span></span>              | <span data-ttu-id="6d6f8-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6d6f8-136">98,765.40</span></span>              | <span data-ttu-id="6d6f8-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-137">98,765.00</span></span>              | <span data-ttu-id="6d6f8-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-138">98,700.00</span></span>                |
| <span data-ttu-id="6d6f8-139">В большую сторону</span><span class="sxs-lookup"><span data-stu-id="6d6f8-139">Rounding-up</span></span>                         | <span data-ttu-id="6d6f8-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6d6f8-140">98,765.43</span></span>              | <span data-ttu-id="6d6f8-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="6d6f8-141">98,765.50</span></span>              | <span data-ttu-id="6d6f8-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-142">98,766.00</span></span>              | <span data-ttu-id="6d6f8-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-143">98,800.00</span></span>                |
| <span data-ttu-id="6d6f8-144">Собственное преимущество, для кредитового сальдо</span><span class="sxs-lookup"><span data-stu-id="6d6f8-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="6d6f8-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6d6f8-145">98,765.43</span></span>              | <span data-ttu-id="6d6f8-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="6d6f8-146">98,765.40</span></span>              | <span data-ttu-id="6d6f8-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-147">98,765.00</span></span>              | <span data-ttu-id="6d6f8-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-148">98,700.00</span></span>                |
| <span data-ttu-id="6d6f8-149">Собственное преимущество, для дебетового сальдо</span><span class="sxs-lookup"><span data-stu-id="6d6f8-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="6d6f8-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6d6f8-150">98,765.43</span></span>              | <span data-ttu-id="6d6f8-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="6d6f8-151">98,765.50</span></span>              | <span data-ttu-id="6d6f8-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-152">98,766.00</span></span>              | <span data-ttu-id="6d6f8-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="6d6f8-154">Без округления, поскольку округление равно 0,00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="6d6f8-155">round(1,0151, 0,00) = 1,0151 round(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="6d6f8-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="6d6f8-156">Обычное округление, и точность округления равна 0,01</span><span class="sxs-lookup"><span data-stu-id="6d6f8-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="6d6f8-157">Округление</span><span class="sxs-lookup"><span data-stu-id="6d6f8-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="6d6f8-158">Процесс расчета</span><span class="sxs-lookup"><span data-stu-id="6d6f8-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6d6f8-159">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="6d6f8-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="6d6f8-160">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="6d6f8-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="6d6f8-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="6d6f8-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6d6f8-162">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="6d6f8-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6d6f8-163">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="6d6f8-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="6d6f8-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="6d6f8-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6d6f8-165">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="6d6f8-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6d6f8-166">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="6d6f8-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="6d6f8-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="6d6f8-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6d6f8-168">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6d6f8-169">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="6d6f8-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="6d6f8-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="6d6f8-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="6d6f8-171">При выборе "Собственное преимущество" округление всегда производится в пользу юридического лица.</span><span class="sxs-lookup"><span data-stu-id="6d6f8-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="6d6f8-172">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6d6f8-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="6d6f8-173">Обзор налога</span><span class="sxs-lookup"><span data-stu-id="6d6f8-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="6d6f8-174">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="6d6f8-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="6d6f8-175">Создание налоговых проводок по документам</span><span class="sxs-lookup"><span data-stu-id="6d6f8-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="6d6f8-176">Просмотр разнесенных налоговых проводок</span><span class="sxs-lookup"><span data-stu-id="6d6f8-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="6d6f8-177">Функция round</span><span class="sxs-lookup"><span data-stu-id="6d6f8-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


