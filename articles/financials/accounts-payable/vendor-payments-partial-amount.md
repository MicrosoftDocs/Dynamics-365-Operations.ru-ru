---
title: "Платежи поставщику на частичную сумму"
description: "Иногда необходимо производить платеж поставщику, который меньше суммы накладной. Эта статья описывает различные варианты для обработки этой ситуации."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2644e0a27eff3e45ddcddb89c9aac9230190788f
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="e2e88-104">Платежи поставщику на частичную сумму</span><span class="sxs-lookup"><span data-stu-id="e2e88-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2e88-105">Иногда необходимо производить платеж поставщику, который меньше суммы накладной.</span><span class="sxs-lookup"><span data-stu-id="e2e88-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="e2e88-106">Эта статья описывает различные варианты для обработки этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="e2e88-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="e2e88-107">Доступные варианты зависят от потребностей и конфигурации бизнеса.</span><span class="sxs-lookup"><span data-stu-id="e2e88-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="e2e88-108">Суммы скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="e2e88-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="e2e88-109">Поставщик может предложить скидку по оплате в случае оплаты по накладной до срока выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2e88-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="e2e88-110">Например, вы вводите накладную на 100,00, которая определяет скидку по оплате в размере 2 процентов, если накладная оплачена в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="e2e88-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="e2e88-111">Условия срока оплаты — 30 дней.</span><span class="sxs-lookup"><span data-stu-id="e2e88-111">The due date terms are 30 days.</span></span> <span data-ttu-id="e2e88-112">Если в предложении по оплате используется скидка по оплате как критерий для выбора накладной и если это предложение выполняется в дату скидки по оплате или до нее, то накладная выбирается для оплаты и создается оплата на 98,00.</span><span class="sxs-lookup"><span data-stu-id="e2e88-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="e2e88-113">Скидку по оплате можно также принять для одноразовой оплаты, которая была создана вручную.</span><span class="sxs-lookup"><span data-stu-id="e2e88-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="e2e88-114">Частичные платежи со скидками по оплате наличными</span><span class="sxs-lookup"><span data-stu-id="e2e88-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="e2e88-115">При выполнении частичного платежа можно запланировать дополнительные частичные платежи для полной оплаты накладной.</span><span class="sxs-lookup"><span data-stu-id="e2e88-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="e2e88-116">Чтобы использовать скидку по оплате для частичной оплаты, нужно установить для параметра **Вычислять скидки по оплате для частичных платежей** значение **Да** на странице **Параметры модуля расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2e88-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="e2e88-117">Например, можно получить скидку по оплате 2%, если накладная оплачивается в течение 10 дней после выставления.</span><span class="sxs-lookup"><span data-stu-id="e2e88-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="e2e88-118">Накладная разнесена для 100,00.</span><span class="sxs-lookup"><span data-stu-id="e2e88-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="e2e88-119">Если сделан платеж на 49,00 в течение 10 дней, в журнал платежей вводится дебет 49,00.</span><span class="sxs-lookup"><span data-stu-id="e2e88-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="e2e88-120">Когда вы сопоставляете частичную оплату на странице **Сопоставление открытых проводок** в поле **Сумма скидки по оплате** появляется **1,00**.</span><span class="sxs-lookup"><span data-stu-id="e2e88-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="e2e88-121">Если ввести частичный платеж и не изменять полную сумму накладной в поле **Сумма сопоставления**, поле **Сумма скидки по оплате** автоматически пересчитывается при разноске проводок.</span><span class="sxs-lookup"><span data-stu-id="e2e88-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="e2e88-122">Кредит-ноты со скидками по оплате</span><span class="sxs-lookup"><span data-stu-id="e2e88-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="e2e88-123">Можно вернуть некоторые номенклатуры, указанные в накладной, и получить кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="e2e88-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="e2e88-124">Если скидка по оплате уже была получена для исходной накладной, можно вычесть значение скидки и получить возмещение верной суммы.</span><span class="sxs-lookup"><span data-stu-id="e2e88-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="e2e88-125">Если для параметра **Вычислять скидки по оплате для кредит-нот** задано значение **Да** на странице **Параметры модуля расчетов с поставщиками**, то скидка автоматически высчитывается для кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="e2e88-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="e2e88-126">Например, можно получить скидку по оплате 2%, если накладная оплачивается в течение 10 дней после выставления.</span><span class="sxs-lookup"><span data-stu-id="e2e88-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="e2e88-127">Накладная разнесена для 100,00.</span><span class="sxs-lookup"><span data-stu-id="e2e88-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="e2e88-128">Если вы возвращаете товары и получаете кредит-ноту, то вы можете ввести кредит-ноту для полной суммы первоначальной накладной (100,00) вместе с 2-процентной скидкой по оплате, которая также определена в кредитовом авизо.</span><span class="sxs-lookup"><span data-stu-id="e2e88-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="e2e88-129">Когда вы просматриваете кредит-ноту на странице **Сопоставление открытых проводок**, в поле **Сумма сопоставления** появляется **98,00** и в поле **Сумма скидки по оплате** появляется **–2,00**.</span><span class="sxs-lookup"><span data-stu-id="e2e88-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="e2e88-130">Сумма скидки разнесена на счет скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="e2e88-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="e2e88-131">Суммы по переплате/недоплате</span><span class="sxs-lookup"><span data-stu-id="e2e88-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="e2e88-132">Вы могли сделать частичную оплату, при которой оставшаяся для сопоставления сумма будет очень небольшой.</span><span class="sxs-lookup"><span data-stu-id="e2e88-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="e2e88-133">Например, сумма по накладной поставщика равна 1 000,00, а вы оплачиваете 999,90.</span><span class="sxs-lookup"><span data-stu-id="e2e88-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="e2e88-134">Если оставшаяся сумма меньше суммы, которая определена для переплат или недоплат на странице **Параметры модуля расчетов с поставщиками**, разница автоматически разносится на счет ГК для переплат и недоплат.</span><span class="sxs-lookup"><span data-stu-id="e2e88-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="e2e88-135">Дополнительные сведения см. в разделе [Обзор платежей поставщикам](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e2e88-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

