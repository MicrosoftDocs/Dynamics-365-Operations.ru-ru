---
title: Скидки по оплате
description: Скидки по оплате настроены и совместно используются для расчетов с клиентами и расчетов с клиентами.  Скидка по оплате можно определить в накладной клиента или накладной поставщика, и будет принята, если накладная оплачивается до даты скидки по оплате.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd15a021244e55ea988a95184a758a321ebeafb3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561623"
---
# <a name="cash-discounts"></a><span data-ttu-id="d10e3-104">Скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="d10e3-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d10e3-105">Скидки по оплате настроены и совместно используются для расчетов с клиентами и расчетов с клиентами.</span><span class="sxs-lookup"><span data-stu-id="d10e3-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="d10e3-106">Скидка по оплате можно определить в накладной клиента или накладной поставщика, и будет принята, если накладная оплачивается до даты скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="d10e3-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="d10e3-107">Скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="d10e3-107">Cash discounts</span></span>

<span data-ttu-id="d10e3-108">Скидки по оплате для обоих клиентов или поставщиков можно создать на странице "Скидки по оплате".</span><span class="sxs-lookup"><span data-stu-id="d10e3-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="d10e3-109">Используя поле "Следующий код скидки", можно также определить серию скидок при оплате наличными, которые сменяют одна другую при истечении срока действия предыдущей скидки по оплате.</span><span class="sxs-lookup"><span data-stu-id="d10e3-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="d10e3-110">Для получения дополнительных сведений см. пример "Серия скидок при оплате наличными" далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d10e3-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="d10e3-111">Если счет, проводка по кредиту (платеж или кредит-нота) или и то, и другое введены в валюте, отличной от валюты учета юридического лица, скидка по оплате рассчитывается с помощью валютного курса на основе даты платежа или кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="d10e3-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="d10e3-112">Если накладная и документ аккредитива вводятся для различных юридических лиц, и если валюты учета для юридических лиц отличаются, валютный курс берется из юридического лица накладной от даты документа аккредитива.</span><span class="sxs-lookup"><span data-stu-id="d10e3-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="d10e3-113">Для получения дополнительных сведений см. пример "Валютные курсы для скидок при оплате наличными" далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d10e3-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="d10e3-114">Порядок по умолчанию счетов ГК для скидки по оплате</span><span class="sxs-lookup"><span data-stu-id="d10e3-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="d10e3-115">Если накладная сопоставлена вовремя для получения скидки при оплате наличными, скидка при оплате наличными автоматически разносится на счет ГК скидок по оплате в соответствии со следующим приоритетом по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="d10e3-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="d10e3-116">Счет ГК, указанный в поле "Альтернативный счет скидок по оплате" на странице "Сопоставление открытых проводок" клиента или на странице "Сопоставление открытых проводок" поставщика.</span><span class="sxs-lookup"><span data-stu-id="d10e3-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="d10e3-117">Счет ГК, указанный в поле "Скидка по оплате по клиенту" или в поле "Скидка по оплате по поставщику" группы разноски ГК, которая назначена налоговому коду накладной.</span><span class="sxs-lookup"><span data-stu-id="d10e3-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="d10e3-118">Настройте группы разноски главной книги на странице "Группы разноски ГК" для налоговых кодов на странице "Налоговые коды".</span><span class="sxs-lookup"><span data-stu-id="d10e3-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="d10e3-119">Счет разноски ГК на странице "Скидки по оплате" в поле "Счет ГК для скидок клиентам" или в поле "Счет ГК для скидок поставщика" для кода скидки по оплате в сопоставленной накладной.</span><span class="sxs-lookup"><span data-stu-id="d10e3-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="d10e3-120">Счет ГК для скидок по оплате, как определено на странице "Счета для автоматических проводок".</span><span class="sxs-lookup"><span data-stu-id="d10e3-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="d10e3-121">Пример. Серия скидок при оплате наличными</span><span class="sxs-lookup"><span data-stu-id="d10e3-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="d10e3-122">Настройте следующие три кода скидок при оплате наличными:</span><span class="sxs-lookup"><span data-stu-id="d10e3-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="d10e3-123">Код 5D10% — скидка 10% при оплате наличными, если сумма оплачивается в течение 5 дней.</span><span class="sxs-lookup"><span data-stu-id="d10e3-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="d10e3-124">Код 10D5% — скидка 5% при оплате наличными, если сумма оплачивается в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="d10e3-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="d10e3-125">Код 14D2% — скидка 2% при оплате наличными, если сумма оплачивается в течение 14 дней.</span><span class="sxs-lookup"><span data-stu-id="d10e3-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="d10e3-126">В поле "Следующий код скидки":</span><span class="sxs-lookup"><span data-stu-id="d10e3-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="d10e3-127">для кода 5D10% выберите 10D5%;</span><span class="sxs-lookup"><span data-stu-id="d10e3-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="d10e3-128">для кода 10D5% выберите 14D2%;</span><span class="sxs-lookup"><span data-stu-id="d10e3-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="d10e3-129">Для кода 14D2% оставьте поле "Следующий код скидки" пустым.</span><span class="sxs-lookup"><span data-stu-id="d10e3-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="d10e3-130">Три скидки по оплате следуют одна за другого по мере того, как дата оплаты становится позже предыдущей даты скидки по оплате накладной.</span><span class="sxs-lookup"><span data-stu-id="d10e3-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="d10e3-131">При оплате накладной предоставляется только одна скидка по оплате, в зависимости от того, какая дата скидки по оплате удовлетворяется в последовательности скидок по оплате.</span><span class="sxs-lookup"><span data-stu-id="d10e3-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="d10e3-132">Пример. Валютные курсы для скидок при оплате наличными</span><span class="sxs-lookup"><span data-stu-id="d10e3-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="d10e3-133">Валюта учета вашего юридического лица — евро, и следующие валютные курсы определены для доллара США:</span><span class="sxs-lookup"><span data-stu-id="d10e3-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="d10e3-134">1 февраля = 110</span><span class="sxs-lookup"><span data-stu-id="d10e3-134">February 1 = 110</span></span>
-   <span data-ttu-id="d10e3-135">1 марта = 80</span><span class="sxs-lookup"><span data-stu-id="d10e3-135">March 1 = 80</span></span>

<span data-ttu-id="d10e3-136">15 февраля разносится накладная на 1000 USD с условиями скидки по оплате 20D2%.</span><span class="sxs-lookup"><span data-stu-id="d10e3-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="d10e3-137">Сумма накладной в валюте учета составляет 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="d10e3-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="d10e3-138">Платеж по накладной в сумме 980 USD сопоставляется 1 марта.</span><span class="sxs-lookup"><span data-stu-id="d10e3-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="d10e3-139">Сумма скидки по оплате равна 20 USD.</span><span class="sxs-lookup"><span data-stu-id="d10e3-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="d10e3-140">Сумма в валюте учета платежа равна 784 евро.</span><span class="sxs-lookup"><span data-stu-id="d10e3-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="d10e3-141">Сумма скидки по оплате в валюте учета рассчитывается с использованием валютного курса на 1 марта: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="d10e3-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="d10e3-142">Если выбран параметр "Вычислять скидки по оплате для частичных платежей" на странице "Параметры модуля расчетов с клиентами" или "Параметры модуля расчетов с поставщиками", используется валютный курс, действующий на дату каждой частичной оплаты.</span><span class="sxs-lookup"><span data-stu-id="d10e3-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

