---
title: "Налоговые платежи и правила округления"
description: "Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: ru-ru
ms.lasthandoff: 08/01/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="c0cf0-103">Налоговые платежи и правила округления</span><span class="sxs-lookup"><span data-stu-id="c0cf0-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c0cf0-104">Эта статья описывает, как работает настройка плавила округления для налоговых органов, а также округление налогового баланса во время выполнения задания сопоставления и разноски налога.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="c0cf0-105">Периодически необходимо сдавать отчеты и уплачивать налоги налоговым ведомствам.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="c0cf0-106">Это может быть сделано путем выполнения процесса сопоставления и разноски налогов на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="c0cf0-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="c0cf0-107">Налог за период будет сопоставлен налоговым счетам, и сальдо налога будет разнесено на счет сопоставления налога.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="c0cf0-108">Сальдо налога, которое разнесено на счет сопоставления налога, может округляться согласно требованиям налоговых ведомств путем настройки правила округления на странице "Налог".</span><span class="sxs-lookup"><span data-stu-id="c0cf0-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="c0cf0-109">Разница округления разносится на счет округления налога, который выбирается в поле "Счета для автоматических проводок" в главной книге.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="c0cf0-110">Приведенный ниже пример иллюстрирует работу правила округления для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="c0cf0-111">Пример:</span><span class="sxs-lookup"><span data-stu-id="c0cf0-111">Example:</span></span>

<span data-ttu-id="c0cf0-112">Полный налог на продажу за период показывает кредитовое сальдо -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="c0cf0-113">Юридическое лицо собрало больше налога, чем уплатило.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="c0cf0-114">Поэтому у юридического лица имеется денежное обязательство перед налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="c0cf0-115">Юридическому лицу необходимо использовать метод округления сальдо до ближайшей кратной 1,00 суммы.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="c0cf0-116">Пользователь, ответственный за учет налогов, должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="c0cf0-117">Нажмите "Налог" &gt; "Косвенные налоги" &gt; "Налог" &gt; "Налоговые органы"</span><span class="sxs-lookup"><span data-stu-id="c0cf0-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="c0cf0-118">На экспресс-вкладке "Общие" выберите значение "Обычный" в поле "Способ округления".</span><span class="sxs-lookup"><span data-stu-id="c0cf0-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="c0cf0-119">В поле "Округление" введите 1,00.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="c0cf0-120">Когда наступит срок уплаты налогов налоговому органу, откройте страницу "Сопоставить и разнести налог".</span><span class="sxs-lookup"><span data-stu-id="c0cf0-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="c0cf0-121">(Нажмите "Налог" &gt; "Объявления" &gt; "Налог" &gt; "Сопоставить и разнести налог".)</span><span class="sxs-lookup"><span data-stu-id="c0cf0-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="c0cf0-122">В счете сопоставления налога сумма налогового обязательства 98 765,43 округляется до 98 765.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="c0cf0-123">В следующей таблице показано, как сумма 98 765,43 округляется с использованием каждого из методов округления, доступных в поле "Способ округления" на странице "Налоговые органы".</span><span class="sxs-lookup"><span data-stu-id="c0cf0-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="c0cf0-124">Параметр способа округления</span><span class="sxs-lookup"><span data-stu-id="c0cf0-124">Rounding form option</span></span>                | <span data-ttu-id="c0cf0-125">Значение округления = 0,01</span><span class="sxs-lookup"><span data-stu-id="c0cf0-125">Round-off value = 0.01</span></span> | <span data-ttu-id="c0cf0-126">Значение округления = 0,10</span><span class="sxs-lookup"><span data-stu-id="c0cf0-126">Round-off value = 0.10</span></span> | <span data-ttu-id="c0cf0-127">Значение округления = 1,00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-127">Round-off value = 1.00</span></span> | <span data-ttu-id="c0cf0-128">Значение округления = 100,00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="c0cf0-129">Обычная</span><span class="sxs-lookup"><span data-stu-id="c0cf0-129">Normal</span></span>                              | <span data-ttu-id="c0cf0-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c0cf0-130">98,765.43</span></span>              | <span data-ttu-id="c0cf0-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c0cf0-131">98,765.40</span></span>              | <span data-ttu-id="c0cf0-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-132">98,765.00</span></span>              | <span data-ttu-id="c0cf0-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-133">98,800.00</span></span>                |
| <span data-ttu-id="c0cf0-134">В меньшую сторону</span><span class="sxs-lookup"><span data-stu-id="c0cf0-134">Downward</span></span>                            | <span data-ttu-id="c0cf0-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c0cf0-135">98,765.43</span></span>              | <span data-ttu-id="c0cf0-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c0cf0-136">98,765.40</span></span>              | <span data-ttu-id="c0cf0-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-137">98,765.00</span></span>              | <span data-ttu-id="c0cf0-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-138">98,700.00</span></span>                |
| <span data-ttu-id="c0cf0-139">В большую сторону</span><span class="sxs-lookup"><span data-stu-id="c0cf0-139">Rounding-up</span></span>                         | <span data-ttu-id="c0cf0-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c0cf0-140">98,765.43</span></span>              | <span data-ttu-id="c0cf0-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="c0cf0-141">98,765.50</span></span>              | <span data-ttu-id="c0cf0-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-142">98,766.00</span></span>              | <span data-ttu-id="c0cf0-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-143">98,800.00</span></span>                |
| <span data-ttu-id="c0cf0-144">Собственное преимущество, для кредитового сальдо</span><span class="sxs-lookup"><span data-stu-id="c0cf0-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="c0cf0-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c0cf0-145">98,765.43</span></span>              | <span data-ttu-id="c0cf0-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="c0cf0-146">98,765.40</span></span>              | <span data-ttu-id="c0cf0-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-147">98,765.00</span></span>              | <span data-ttu-id="c0cf0-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-148">98,700.00</span></span>                |
| <span data-ttu-id="c0cf0-149">Собственное преимущество, для дебетового сальдо</span><span class="sxs-lookup"><span data-stu-id="c0cf0-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="c0cf0-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="c0cf0-150">98,765.43</span></span>              | <span data-ttu-id="c0cf0-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="c0cf0-151">98,765.50</span></span>              | <span data-ttu-id="c0cf0-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-152">98,766.00</span></span>              | <span data-ttu-id="c0cf0-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="c0cf0-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="c0cf0-154">При выборе "Собственное преимущество" округление всегда производится в пользу юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="c0cf0-155">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c0cf0-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="c0cf0-156">Обзор налога</span><span class="sxs-lookup"><span data-stu-id="c0cf0-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="c0cf0-157">Создание налогового платежа</span><span class="sxs-lookup"><span data-stu-id="c0cf0-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="c0cf0-158">Создание налоговых проводок по документам</span><span class="sxs-lookup"><span data-stu-id="c0cf0-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="c0cf0-159">Просмотр разнесенных налоговых проводок</span><span class="sxs-lookup"><span data-stu-id="c0cf0-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



