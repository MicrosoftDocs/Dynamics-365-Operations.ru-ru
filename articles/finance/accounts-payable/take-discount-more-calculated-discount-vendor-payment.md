---
title: Использование скидки, превышающей вычисленную скидку для платежа поставщика
description: В этой статье рассматривается сценарий, в котором скидка по оплате используется для суммы, которая превышает скидку, первоначально доступную для накладной. Такая ситуация может возникнуть, если организация пришла с поставщиком к соглашению о том, что сумма оплаты по накладной будет снижена.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810254"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="8cfbf-104">Использование скидки, превышающей вычисленную скидку для платежа поставщика</span><span class="sxs-lookup"><span data-stu-id="8cfbf-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cfbf-105">В этой статье рассматривается сценарий, в котором скидка по оплате используется для суммы, которая превышает скидку, первоначально доступную для накладной.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="8cfbf-106">Такая ситуация может возникнуть, если организация пришла с поставщиком к соглашению о том, что сумма оплаты по накладной будет снижена.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="8cfbf-107">Поставщик 3051 предоставляет Fabrikam скидку на оплату в размере 4 %, если счет будет оплачен в течение 7 дней.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="8cfbf-108">29 июня Эйприл вводит счет на 1 000,00 в систему.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="8cfbf-109">Поставщик позволяет Эйприл использовать скидку 60,00 вместо скидки по умолчанию 40,00, доступной для данного счета.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="8cfbf-110">Эйприл записывает одноразовую оплату путем использования журнала платежей по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="8cfbf-111">Она вводит поставщика для платежа, после этого открывает страницу **Сопоставление проводок**.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="8cfbf-112">Она отмечает накладную и изменяет значение в поле **Сумма скидки по оплате** на **60,00**.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="8cfbf-113">Пометка</span><span class="sxs-lookup"><span data-stu-id="8cfbf-113">Mark</span></span>     | <span data-ttu-id="8cfbf-114">Использовать скидку по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-114">Use cash discount</span></span> | <span data-ttu-id="8cfbf-115">Операция</span><span class="sxs-lookup"><span data-stu-id="8cfbf-115">Voucher</span></span>   | <span data-ttu-id="8cfbf-116">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="8cfbf-116">Account</span></span> | <span data-ttu-id="8cfbf-117">Дата</span><span class="sxs-lookup"><span data-stu-id="8cfbf-117">Date</span></span>      | <span data-ttu-id="8cfbf-118">Срок выполнения</span><span class="sxs-lookup"><span data-stu-id="8cfbf-118">Due date</span></span>  | <span data-ttu-id="8cfbf-119">Счет</span><span class="sxs-lookup"><span data-stu-id="8cfbf-119">Invoice</span></span> | <span data-ttu-id="8cfbf-120">Сумма в валюте проводки</span><span class="sxs-lookup"><span data-stu-id="8cfbf-120">Amount in transaction currency</span></span> | <span data-ttu-id="8cfbf-121">Валютное</span><span class="sxs-lookup"><span data-stu-id="8cfbf-121">Currency</span></span> | <span data-ttu-id="8cfbf-122">Сумма сопоставления</span><span class="sxs-lookup"><span data-stu-id="8cfbf-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="8cfbf-123">Выбрано</span><span class="sxs-lookup"><span data-stu-id="8cfbf-123">Selected</span></span> | <span data-ttu-id="8cfbf-124">Обычная</span><span class="sxs-lookup"><span data-stu-id="8cfbf-124">Normal</span></span>            | <span data-ttu-id="8cfbf-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="8cfbf-125">Inv-10040</span></span> | <span data-ttu-id="8cfbf-126">3051</span><span class="sxs-lookup"><span data-stu-id="8cfbf-126">3051</span></span>    | <span data-ttu-id="8cfbf-127">29.06.2015</span><span class="sxs-lookup"><span data-stu-id="8cfbf-127">6/29/2015</span></span> | <span data-ttu-id="8cfbf-128">29.07.2015</span><span class="sxs-lookup"><span data-stu-id="8cfbf-128">7/29/2015</span></span> | <span data-ttu-id="8cfbf-129">10040</span><span class="sxs-lookup"><span data-stu-id="8cfbf-129">10040</span></span>   | <span data-ttu-id="8cfbf-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8cfbf-130">1,000.00</span></span>                       | <span data-ttu-id="8cfbf-131">американский доллар</span><span class="sxs-lookup"><span data-stu-id="8cfbf-131">USD</span></span>      | <span data-ttu-id="8cfbf-132">940,00</span><span class="sxs-lookup"><span data-stu-id="8cfbf-132">940.00</span></span>           |

<span data-ttu-id="8cfbf-133">Данные по скидкам появляются внизу страницы **Сопоставление проводок**.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="8cfbf-134">Поле</span><span class="sxs-lookup"><span data-stu-id="8cfbf-134">Field</span></span>                        | <span data-ttu-id="8cfbf-135">значение</span><span class="sxs-lookup"><span data-stu-id="8cfbf-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="8cfbf-136">Дата скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-136">Cash discount date</span></span>           | <span data-ttu-id="8cfbf-137">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="8cfbf-137">7/12/2015</span></span> |
| <span data-ttu-id="8cfbf-138">Сумма скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-138">Cash discount amount</span></span>         | <span data-ttu-id="8cfbf-139">60.00</span><span class="sxs-lookup"><span data-stu-id="8cfbf-139">60.00</span></span>     |
| <span data-ttu-id="8cfbf-140">Использовать скидку по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-140">Use cash discount</span></span>            | <span data-ttu-id="8cfbf-141">Обычная</span><span class="sxs-lookup"><span data-stu-id="8cfbf-141">Normal</span></span>    |
| <span data-ttu-id="8cfbf-142">Скидка по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-142">Cash discount taken</span></span>          | <span data-ttu-id="8cfbf-143">0,00</span><span class="sxs-lookup"><span data-stu-id="8cfbf-143">0.00</span></span>      |
| <span data-ttu-id="8cfbf-144">Сумма скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="8cfbf-144">Cash discount amount to take</span></span> | <span data-ttu-id="8cfbf-145">60,00</span><span class="sxs-lookup"><span data-stu-id="8cfbf-145">60.00</span></span>     |

<span data-ttu-id="8cfbf-146">Эйприл разносил журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-146">April posts the payment journal.</span></span> <span data-ttu-id="8cfbf-147">Счет полностью сопоставлен с платежом 940,00 и скидкой 60,00.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]