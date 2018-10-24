---
title: "Налог на добавленную стоимость (НДС) для налоговых агентов (Россия)"
description: "В этой теме поясняется, как настроить НДС и выполнять проводки для налогового агента для России."
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, VATOperationCodeTable_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 5bc54f699605b9fb313fede70dd1f3fb0dcc8873
ms.contentlocale: ru-ru
ms.lasthandoff: 10/01/2018

---
# <a name="value-added-tax-vat-for-tax-agents-russia"></a><span data-ttu-id="556ad-103">Налог на добавленную стоимость (НДС) для налоговых агентов (Россия)</span><span class="sxs-lookup"><span data-stu-id="556ad-103">Value-added tax (VAT) for tax agents (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="556ad-104">Когда компания признается налоговым агентом, она должна правильно начислять и вычитать налог на добавленную стоимость (НДС) из сумм, выплачиваемых налогоплательщикам, или начислять НДС за счет собственных средств.</span><span class="sxs-lookup"><span data-stu-id="556ad-104">When a company is acknowledged as a tax agent, it must correctly accrue and deduct value-added tax (VAT) from funds that are paid to taxpayers, or it must accrue VAT at the expense of its own funds.</span></span> <span data-ttu-id="556ad-105">Затем она должна переводить НДС налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="556ad-105">It must then transfer VAT to the tax authority.</span></span>

<span data-ttu-id="556ad-106">Такая функциональная возможность необходима для создания накладных, счетов-фактур и платежей поставщикам, для которых компания определена в качестве налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-106">This functionality is required in order to generate invoices, factures, and payments to vendors that the company is defined as a tax agent (fiscal agent) for.</span></span>

<span data-ttu-id="556ad-107">Поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="556ad-107">The following functions are supported:</span></span>

- <span data-ttu-id="556ad-108">Создание поставщиков, для которых ваша компания выступает в качестве налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-108">Create vendors that your company operates as a tax agent for.</span></span>
- <span data-ttu-id="556ad-109">Пометка налоговых кодов для проводок налогового агента для указания того, как должна происходить уплата НДС: из средств поставщика или за счет собственных средств компании.</span><span class="sxs-lookup"><span data-stu-id="556ad-109">Mark sales tax codes for tax agent transactions to specify whether the VAT payments must be made from the vendor's funds or at the expense of your company's own funds.</span></span>
- <span data-ttu-id="556ad-110">Создание предложений по оплате для накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="556ad-110">Create payment proposals for vendor invoices.</span></span>
- <span data-ttu-id="556ad-111">Создание платежей для налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="556ad-111">Create payments for tax authorities.</span></span>
- <span data-ttu-id="556ad-112">Разноска и сопоставление платежей поставщику.</span><span class="sxs-lookup"><span data-stu-id="556ad-112">Post and settle payments to the vendor.</span></span>
- <span data-ttu-id="556ad-113">Создание и печать счетов-фактур на сумму НДС, которая должна быть перечислена налоговым органам, и регистрация счетов-фактур в книге продаж.</span><span class="sxs-lookup"><span data-stu-id="556ad-113">Create and print factures for the VAT amount that is to be remitted to tax authorities, and register the factures in the sales book</span></span> 
- <span data-ttu-id="556ad-114">Регистрация счетов-фактур для вычета НДС в книге покупок.</span><span class="sxs-lookup"><span data-stu-id="556ad-114">Register factures for VAT deduction in the purchase book.</span></span>

## <a name="set-up-tax-agent-transactions"></a><span data-ttu-id="556ad-115">Настройка проводок налогового агента</span><span class="sxs-lookup"><span data-stu-id="556ad-115">Set up tax agent transactions</span></span>

<span data-ttu-id="556ad-116">Прежде чем создавать проводки налогового агента, необходимо настроить параметры для них в модуле **Налог**.</span><span class="sxs-lookup"><span data-stu-id="556ad-116">Before you can create tax agent transactions, you must set up the parameters for them in the **Tax** module.</span></span>

### <a name="set-up-the-vat-operation-code-for-the-tax-declaration"></a><span data-ttu-id="556ad-117">Настройка кода операции по НДС для налоговой декларации</span><span class="sxs-lookup"><span data-stu-id="556ad-117">Set up the VAT operation code for the tax declaration</span></span>

1. <span data-ttu-id="556ad-118">Выберите **Налог** \> **Настройка** \> **Налог** \> **Коды операций по НДС**.</span><span class="sxs-lookup"><span data-stu-id="556ad-118">Select **Tax** \> **Setup** \> **Sales tax** \> **VAT operation codes**.</span></span>
2. <span data-ttu-id="556ad-119">В поле **Код операции по НДС** введите код операции для декларации по НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-119">In the **VAT operation code** field, enter the operation code for the VAT declaration.</span></span>
3. <span data-ttu-id="556ad-120">В поле **Описание** введите описание для кода проводки.</span><span class="sxs-lookup"><span data-stu-id="556ad-120">In the **Description** field, enter a description for the transaction code.</span></span>
4. <span data-ttu-id="556ad-121">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-121">Press Ctrl+S, or close the page.</span></span>

### <a name="set-up-the-sales-tax-code-for-tax-agent-transactions"></a><span data-ttu-id="556ad-122">Настройка налогового кода для проводок налогового агента</span><span class="sxs-lookup"><span data-stu-id="556ad-122">Set up the sales tax code for tax agent transactions</span></span>

1. <span data-ttu-id="556ad-123">Выберите **Косвенные налоги** \> **Налог** \> **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="556ad-123">Select **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="556ad-124">Нажмите CTRL+N, чтобы создать налоговый код.</span><span class="sxs-lookup"><span data-stu-id="556ad-124">Press Ctrl+N to create a tax code.</span></span>
3. <span data-ttu-id="556ad-125">В поле **Налоговый код** введите код для налога.</span><span class="sxs-lookup"><span data-stu-id="556ad-125">In the **Sales tax code** field, enter a code for sales tax.</span></span>
4. <span data-ttu-id="556ad-126">В поле **Период сопоставления** выберите период, за который рассчитывается налог и уплачивается налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="556ad-126">In the **Settlement period** field, select the period that the tax is calculated and paid to the tax authority for.</span></span>
5. <span data-ttu-id="556ad-127">В поле **Группа разноски ГК** выберите группу разноски ГК для выбранного налогового кода.</span><span class="sxs-lookup"><span data-stu-id="556ad-127">In the **Ledger posting group** field, select the ledger posting group for the sales tax code.</span></span>
6. <span data-ttu-id="556ad-128">В поле **Тип налога** выберите **Стандартный НДС** или **Пониженный НДС**.</span><span class="sxs-lookup"><span data-stu-id="556ad-128">In the **Type of tax** field, select either **Standard VAT** or **Reduced VAT**.</span></span>
7. <span data-ttu-id="556ad-129">В поле **Начисление НДС** выберите источник начисления НДС:</span><span class="sxs-lookup"><span data-stu-id="556ad-129">In the **VAT charge** field, select the source of VAT accrual:</span></span>

    - <span data-ttu-id="556ad-130">**Из средств поставщика** — выплата НДС производится из дохода поставщика.</span><span class="sxs-lookup"><span data-stu-id="556ad-130">**From vendor funds** − The VAT payment is made from the vendor's income.</span></span>
    - <span data-ttu-id="556ad-131">**Из собственных средств** — выплата НДС производится из средств налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-131">**From own funds** − The VAT payment is made from the tax agent's funds.</span></span>

8. <span data-ttu-id="556ad-132">Выберите **Значения**, чтобы открыть страницу **Значения**.</span><span class="sxs-lookup"><span data-stu-id="556ad-132">Select **Values** to open the **Values** page.</span></span>
9. <span data-ttu-id="556ad-133">В поле **Значение** введите процент НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-133">In the **Value** field, enter the VAT percentage.</span></span>
10. <span data-ttu-id="556ad-134">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-134">Press Ctrl+S, or close the page.</span></span>
11. <span data-ttu-id="556ad-135">Выберите **Косвенные налоги** \> **Налог** \> **Налоговые группы**.</span><span class="sxs-lookup"><span data-stu-id="556ad-135">Select **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
12. <span data-ttu-id="556ad-136">Нажмите CTRL+N, чтобы создать налоговую группу, а затем введите необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-136">Press Ctrl+N to create a sales tax group, and enter the required information.</span></span>
13. <span data-ttu-id="556ad-137">На вкладке **Настройка**, в поле **Налоговый код** выберите налоговый код, созданный на шагах 1–10.</span><span class="sxs-lookup"><span data-stu-id="556ad-137">On the **Setup** tab, in the **Sales tax code** field, select the sales tax code that you created in steps 1 through 10.</span></span>

    > [!NOTE]
    > <span data-ttu-id="556ad-138">Если вы выбрали вариант **Из собственных средств** для налогового кода на шаге 7, по умолчанию устанавливается флажок **Налоговое освобождение** на вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="556ad-138">If you selected the **From own funds** option for the sales tax code in step 7, the **Exempt** option is selected by default on the **Setup** tab.</span></span>

14. <span data-ttu-id="556ad-139">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-139">Press Ctrl+S, or close the page.</span></span>
15. <span data-ttu-id="556ad-140">Выберите **Косвенные налоги** \> **Налог** \> **Налоговые группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="556ad-140">Select **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
16. <span data-ttu-id="556ad-141">Нажмите CTRL+N, чтобы создать налоговую группу номенклатур, а затем введите необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-141">Press Ctrl+N to create an item sales tax group, and enter the required information.</span></span> 
17. <span data-ttu-id="556ad-142">На вкладке **Настройка**, в поле **Налоговый код** выберите налоговый код, созданный на шагах 1–10.</span><span class="sxs-lookup"><span data-stu-id="556ad-142">On the **Setup** tab, in the **Sales tax code** field, select the sales tax code that you created in steps 1 through 10.</span></span>
18. <span data-ttu-id="556ad-143">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-143">Press Ctrl+S, or close the page.</span></span>

### <a name="set-up-a-vendor-tax-authority"></a><span data-ttu-id="556ad-144">Настройка налогового органа поставщика</span><span class="sxs-lookup"><span data-stu-id="556ad-144">Set up a vendor tax authority</span></span>

1. <span data-ttu-id="556ad-145">Выберите **Косвенные налоги** \> **Налог** \> **Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="556ad-145">Select **Indirect taxes** \> **Sales tax** \> **Sales tax authorities**.</span></span>
2. <span data-ttu-id="556ad-146">Нажмите CTRL+N, чтобы создать налоговый орган, а затем введите необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-146">Press Ctrl+N to create a tax authority, and enter the required information.</span></span>
3. <span data-ttu-id="556ad-147">В поле **Счет поставщика** выберите поставщика, который выступает в качестве налогового органа.</span><span class="sxs-lookup"><span data-stu-id="556ad-147">In the **Vendor account** field, select the vendor that operates as the tax authority.</span></span>
4. <span data-ttu-id="556ad-148">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-148">Press Ctrl+S, or close the page.</span></span>

## <a name="create-a-vendor-that-your-company-acts-as-a-tax-agent-for-and-post-transactions"></a><span data-ttu-id="556ad-149">Создание поставщика, для которого ваша компания выступает в качестве налогового агента, и разноска проводок</span><span class="sxs-lookup"><span data-stu-id="556ad-149">Create a vendor that your company acts as a tax agent for, and post transactions</span></span>

<span data-ttu-id="556ad-150">На странице **Поставщики** можно определить поставщика в качестве налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-150">On the **Vendors** page, you can define a vendor as a tax agent.</span></span> <span data-ttu-id="556ad-151">После этого можно совершать транзакции с этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="556ad-151">You can then perform transactions with this vendor.</span></span>

1. <span data-ttu-id="556ad-152">Выберите **Расчеты с поставщиками** \> **Поставщики** \> **Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="556ad-152">Select **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="556ad-153">Нажмите Ctrl + N, чтобы создать поставщика, для которого ваша компания выступает в качестве налогового агента, и введите необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-153">Press Ctrl+N to create a vendor that your company acts as a tax agent for, and enter the required information.</span></span>
3. <span data-ttu-id="556ad-154">На вкладке **Общее** установите для параметра **Налоговый агент** значение **Да**, чтобы определить поставщика как налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-154">On the **General** tab, set the **Tax agent** option to **Yes** to define the vendor as a tax agent.</span></span>
4. <span data-ttu-id="556ad-155">В поле **Тип поставщика** выберите тип поставщика:</span><span class="sxs-lookup"><span data-stu-id="556ad-155">In the **Vendor type** field, select the type of vendor:</span></span>

    - <span data-ttu-id="556ad-156">**Пустое поле** — поставщик является обычным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="556ad-156">**Blank** – The vendor is a common vendor.</span></span>
    - <span data-ttu-id="556ad-157">**Нерезидент** — Поставщик — иностранец.</span><span class="sxs-lookup"><span data-stu-id="556ad-157">**Non resident** – The vendor is a foreigner.</span></span>
    - <span data-ttu-id="556ad-158">**Государственный орган** — Поставщик — правительственная или муниципальная организация.</span><span class="sxs-lookup"><span data-stu-id="556ad-158">**State authority** – The vendor is a governmental or municipal authority.</span></span>

5. <span data-ttu-id="556ad-159">В поле **Код операции по НДС** выберите код операции для декларации по НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-159">In the **VAT operation code** field, select the operation code for the VAT declaration.</span></span>
6. <span data-ttu-id="556ad-160">Нажмите CTRL+S или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="556ad-160">Press Ctrl+S, or close the page.</span></span>
7. <span data-ttu-id="556ad-161">Выберите **Расчеты с поставщиками** \> **Заказы на покупку** \> **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="556ad-161">Select **Accounts payable** \> **Purchase orders** \> **All purchase orders**.</span></span>
8. <span data-ttu-id="556ad-162">Нажмите CTRL+N, чтобы создать заказ на покупку для поставщика, и введите необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-162">Press Ctrl+N to create a purchase order for the vendor, and enter the required information.</span></span>
9. <span data-ttu-id="556ad-163">Выберите **Заголовок** чтобы открыть представление заголовка, а затем на вкладке **Настройка** в поле **Код операции по НДС** просмотрите или измените код для декларации по НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-163">Select **Header** to open the Header view, and then, on the **Setup** tab, in the **VAT operation code** field, view or modify the code for the VAT declaration.</span></span>
10. <span data-ttu-id="556ad-164">В поле **Начисление НДС** выберите источник начисления НДС: **Из средств поставщика** или **Из собственных средств**.</span><span class="sxs-lookup"><span data-stu-id="556ad-164">In the **VAT charge** field, select the source of VAT accrual: **From vendor funds** or **From own funds**.</span></span>
11. <span data-ttu-id="556ad-165">Подтвердите заказ на покупку и разнесите накладную.</span><span class="sxs-lookup"><span data-stu-id="556ad-165">Confirm the purchase order, and post the invoice.</span></span>

## <a name="create-tax-payments"></a><span data-ttu-id="556ad-166">Создание налоговых платежей</span><span class="sxs-lookup"><span data-stu-id="556ad-166">Create tax payments</span></span>

<span data-ttu-id="556ad-167">В журнале платежей поставщикам реализованы два варианта уплаты НДС в качестве налогового агента:</span><span class="sxs-lookup"><span data-stu-id="556ad-167">In the Vendor payment journal, two options for paying VAT as a tax agent are implemented:</span></span>

- <span data-ttu-id="556ad-168">Уплата по выбранной накладной</span><span class="sxs-lookup"><span data-stu-id="556ad-168">Payment for a specific invoice</span></span>
- <span data-ttu-id="556ad-169">Предоплата (накладная неизвестна)</span><span class="sxs-lookup"><span data-stu-id="556ad-169">Prepayment (invoice is unknown)</span></span>

### <a name="create-a-payment-proposal-for-a-tax-agent-invoice"></a><span data-ttu-id="556ad-170">Создание предложения по оплате для накладной налогового агента</span><span class="sxs-lookup"><span data-stu-id="556ad-170">Create a payment proposal for a tax agent invoice</span></span>

<span data-ttu-id="556ad-171">На странице **Предложение по оплате от поставщика** можно создавать предложения по оплате, которые можно использовать для формирования платежей поставщику-налоговому агенту.</span><span class="sxs-lookup"><span data-stu-id="556ad-171">On the **Vendor payment proposal** page, you can create payment proposals that you can use to generate payments to a vendor tax agent.</span></span> <span data-ttu-id="556ad-172">Можно также формировать выплаты НДС налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="556ad-172">You can also generate VAT payments to a tax authority.</span></span>

1. <span data-ttu-id="556ad-173">Выберите **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="556ad-173">Select **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="556ad-174">Нажмите CTRL+N, чтобы создать журнал, а затем выберите **Строки**, чтобы открыть страницу **Платежи поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="556ad-174">Press Ctrl+N to create a journal, and then select **Lines** to open the **Vendor payments** page.</span></span>
3. <span data-ttu-id="556ad-175">Выберите **Предложение по оплате** \> **Создать предложение по оплате**, чтобы открыть страницу **Предложение по оплате от поставщика**.</span><span class="sxs-lookup"><span data-stu-id="556ad-175">Select **Payment proposal** \> **Create payment proposal** to open the **Vendor payment proposal** page.</span></span>
4. <span data-ttu-id="556ad-176">В поле **Выбрать накладные по** выберите тип предложения по оплате, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="556ad-176">In the **Select invoices by** field, select the type of payment proposal to create.</span></span> <span data-ttu-id="556ad-177">Предложение можно создать по дате оплаты, дате скидки за оплату наличными, или и по дате оплаты, и по дате скидки за оплату наличными.</span><span class="sxs-lookup"><span data-stu-id="556ad-177">You can create the proposal by due date, by cash discount date, or by both due date and cash discount date.</span></span>
5. <span data-ttu-id="556ad-178">Выберите **Включаемые записи**, а затем выберите **Фильтр**, чтобы определить критерии для предложения по оплате.</span><span class="sxs-lookup"><span data-stu-id="556ad-178">Select **Records to include**, and then select **Filter** to define the criteria for the payment proposal.</span></span> <span data-ttu-id="556ad-179">Например, можно использовать в качестве критерия счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="556ad-179">For example, you can use the vendor account as a criterion.</span></span>
6. <span data-ttu-id="556ad-180">Выберите **OK**, чтобы открыть страницу **Предложение по оплате от поставщика**.</span><span class="sxs-lookup"><span data-stu-id="556ad-180">Select **OK** to open the **Vendor payment proposal** page.</span></span> <span data-ttu-id="556ad-181">В верхней области можно просмотреть открытые проводки по накладным, которые вносят свой вклад в строку предложения по оплате.</span><span class="sxs-lookup"><span data-stu-id="556ad-181">In the upper pane, you can view the open invoice transactions that contribute to the payment proposal line.</span></span> <span data-ttu-id="556ad-182">На вкладке **Предложение по НДС** можно просмотреть сведения о налоговой проводке по уплате НДС налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="556ad-182">On the **VAT Proposal** tab, you can view the details of the tax transaction for the VAT payment to the tax authorities.</span></span>
7. <span data-ttu-id="556ad-183">Выберите **Создать платежи**, чтобы перенести строки предложения в журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="556ad-183">Select **Create payments** to transfer the proposal lines to the payment journal.</span></span>

    <span data-ttu-id="556ad-184">На странице **Платежи поставщикам** отображается по две строки платежа для каждой накладной.</span><span class="sxs-lookup"><span data-stu-id="556ad-184">The **Vendor payments** page shows two payment lines for each invoice.</span></span> <span data-ttu-id="556ad-185">Одна строка — это платеж поставщику, а другая — налоговый платеж в налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="556ad-185">One line is for a payment to a vendor, and the other line is for a tax payment to a tax authority.</span></span> <span data-ttu-id="556ad-186">На второй строке журнала в поле **Назначение платежа** отображается назначение платежа НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-186">On the second journal line, the **Purpose text** field shows the purpose of the VAT payment.</span></span> <span data-ttu-id="556ad-187">Также отображаются номер счета и адрес поставщика.</span><span class="sxs-lookup"><span data-stu-id="556ad-187">The vendor account number and address are included.</span></span>

    > [!NOTE]
    > <span data-ttu-id="556ad-188">Для строки, которая представляет собой налоговый платеж в налоговый орган, в поле **Налоговый код** на вкладке **Общие** отображается налоговый код.</span><span class="sxs-lookup"><span data-stu-id="556ad-188">For the line that is a tax payment to a tax authority, the **Sales tax code** field on the **General** tab shows the sales tax code.</span></span> <span data-ttu-id="556ad-189">В поле **Счет поставщика** на вкладке **Платеж** отображается счет поставщика, за которого уплачивается налог.</span><span class="sxs-lookup"><span data-stu-id="556ad-189">The **Vendor account** field on the **Payment** tab shows the vendor account that the tax is paid for.</span></span>

8. <span data-ttu-id="556ad-190">В поле **Код операции по НДС** просмотрите или измените код операции для декларации по НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-190">In the **VAT operation code** field, view or modify the operation code for the VAT declaration.</span></span>
9. <span data-ttu-id="556ad-191">Выберите **Создание платежей**, чтобы открыть страницу **Создание платежей**.</span><span class="sxs-lookup"><span data-stu-id="556ad-191">Select **Generate payments** to open the **Generate payments** page.</span></span>
10. <span data-ttu-id="556ad-192">Выберите способ оплаты или формат экспорта в зависимости от метода платежа, указанного в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="556ad-192">Select either the payment method or the export format, depending on the method of payment on the journal line.</span></span> <span data-ttu-id="556ad-193">Выберите банковский счет для осуществления платежа и введите нужную информацию.</span><span class="sxs-lookup"><span data-stu-id="556ad-193">Then select the bank account to draw the payment from, and enter the required information.</span></span> 
11. <span data-ttu-id="556ad-194">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="556ad-194">Select **OK**.</span></span>
12. <span data-ttu-id="556ad-195">Выберите **Печать**\>**Платежное поручение**, чтобы распечатать отчет о платежном поручении.</span><span class="sxs-lookup"><span data-stu-id="556ad-195">Select **Print** \> **Payment order** to print the payment order report.</span></span>
13. <span data-ttu-id="556ad-196">На странице **Ваучер журнала** выберите **Проверить** \> **Проверить**, чтобы проверить строку журнала.</span><span class="sxs-lookup"><span data-stu-id="556ad-196">On the **Journal voucher** page, select **Validate** \> **Validate** to validate the journal line.</span></span> <span data-ttu-id="556ad-197">Затем выберите **Разнести** \> **Разнести** , чтобы разнести строки журнала.</span><span class="sxs-lookup"><span data-stu-id="556ad-197">Then select **Post** \> **Post** to post the journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="556ad-198">После того как платежи налоговому агенту поставщика совершены, можно просмотреть сопоставленные проводки на странице **Проводки по сопоставлению**.</span><span class="sxs-lookup"><span data-stu-id="556ad-198">After payments to the vendor are completed, you can view the settled transactions on the **Transactions on settlement** page.</span></span> <span data-ttu-id="556ad-199">Просмотреть разнесенные налоговые проводки можно на странице **Налоговые проводки**.</span><span class="sxs-lookup"><span data-stu-id="556ad-199">You can view the posted sales tax transactions on the **Sales tax transactions** page.</span></span>

### <a name="create-a-prepayment"></a><span data-ttu-id="556ad-200">Создание предоплаты</span><span class="sxs-lookup"><span data-stu-id="556ad-200">Create a prepayment</span></span>

1. <span data-ttu-id="556ad-201">Выберите **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="556ad-201">Select **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="556ad-202">Нажмите CTRL+N, чтобы создать журнал, а затем выберите **Строки**, чтобы открыть страницу **Платежи поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="556ad-202">Press Ctrl+N to create a journal, and then select **Lines** to open the **Vendor payments** page.</span></span>
3. <span data-ttu-id="556ad-203">Нажмите CTRL+N, чтобы создать новую строку журнала, выберите поставщика и введите сумму предоплаты.</span><span class="sxs-lookup"><span data-stu-id="556ad-203">Press Ctrl+N to create a new journal line, select the vendor, and enter a prepayment amount.</span></span>
4. <span data-ttu-id="556ad-204">Укажите налоговую группу и налоговую группу номенклатур, содержащие налоговый код с необходимой настройкой начисления НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-204">Specify the sales tax group and item sales tax group that contain the sales tax code that has the required setup of the VAT charge.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="556ad-205">Подлежащая уплате сумма НДС рассчитывается на основании значения налогового кода.</span><span class="sxs-lookup"><span data-stu-id="556ad-205">The VAT amount that must be paid is calculated based on the value of the sales tax code.</span></span>
    > - <span data-ttu-id="556ad-206">Чтобы запретить расчет налога на саму предоплату, на странице **Параметры модуля расчетов с поставщиками** на вкладке **Главная книга и налог** установите для параметра **Налог по предоплате в журнале платежей** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="556ad-206">To prevent tax from being calculated on the prepayment itself, on the **Accounts payable parameters** page, on the **Ledger and sales tax** tab, set the **Sales tax on prepayment in payment journal** option to **No**.</span></span>

5. <span data-ttu-id="556ad-207">Выберите **Предложение по оплате** \> **Предложение по НДС**.</span><span class="sxs-lookup"><span data-stu-id="556ad-207">Select **Payment proposal** \> **VAT Proposal**.</span></span> <span data-ttu-id="556ad-208">Созданная строка налогового платежа включает информацию о налоговом коде, код операции по НДС и поставщика, за которого вы уплачиваете налог.</span><span class="sxs-lookup"><span data-stu-id="556ad-208">The tax payment line that is created includes information about the tax code, the VAT operation code, and the supplier that you pay the tax for.</span></span>
 

## <a name="create-and-print-factures-for-vat-deductions"></a><span data-ttu-id="556ad-209">Создание и печать счетов-фактур для вычетов НДС</span><span class="sxs-lookup"><span data-stu-id="556ad-209">Create and print factures for VAT deductions</span></span>

<span data-ttu-id="556ad-210">Прежде чем можно будет создать и распечатать отчет о счетах-фактурах для полученных накладных, выпущенных накладных, покупок или продаж в оценках НДС, необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="556ad-210">Before you can create and print a facture report for received invoices, issued invoices, purchases, or sales in estimates of VAT, you must complete the following tasks.</span></span>

1. <span data-ttu-id="556ad-211">Настройте параметры проводок налоговых агентов.</span><span class="sxs-lookup"><span data-stu-id="556ad-211">Set up the parameters for a tax agent transaction.</span></span>
2. <span data-ttu-id="556ad-212">Определите поставщика в качестве налогового агента.</span><span class="sxs-lookup"><span data-stu-id="556ad-212">Define a vendor as a tax agent.</span></span>
3. <span data-ttu-id="556ad-213">Создайте и разнесите заказ на покупку с налоговой группой и налоговой группой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="556ad-213">Create and post a purchase order that has a sales tax group and an item sales tax group.</span></span>
4. <span data-ttu-id="556ad-214">Создайте предложение по оплате и разнесите платеж.</span><span class="sxs-lookup"><span data-stu-id="556ad-214">Create a payment proposal, and post the payment.</span></span>

    <span data-ttu-id="556ad-215">В результате разноски налогового платежа создаются налоговые проводки со следующими направлениями налога:</span><span class="sxs-lookup"><span data-stu-id="556ad-215">As a result of tax payment posting, sales tax transactions are created that have the following tax directions:</span></span>

    - <span data-ttu-id="556ad-216">**Налоговый агент - начислено** — начисленный НДС, который должен быть уплачен.</span><span class="sxs-lookup"><span data-stu-id="556ad-216">**Tax agent – charged** – Accrued VAT that must be paid.</span></span> <span data-ttu-id="556ad-217">По этой налоговой проводке создается документ-фактура, который будет отражен в книге продаж.</span><span class="sxs-lookup"><span data-stu-id="556ad-217">A facture document is created on this sales tax transaction and will be reflected in the sales book.</span></span>
    - <span data-ttu-id="556ad-218">**Входящий налог** — НДС, который следует вычесть, потому что сумма НДС была переведена налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="556ad-218">**Sales tax receivable** – VAT that must be deducted because the VAT amount was transferred to the tax authority.</span></span> <span data-ttu-id="556ad-219">По налоговой проводке создается счет-фактура, который будет отражен в книге покупок после обработки входящего НДС.</span><span class="sxs-lookup"><span data-stu-id="556ad-219">The facture is created on the sales tax transaction and will be reflected in the purchase book after VAT incoming is processed.</span></span>

5. <span data-ttu-id="556ad-220">Выберите **Расчеты с поставщиками** \> **Запросы и отчеты** \> **Фактура**.</span><span class="sxs-lookup"><span data-stu-id="556ad-220">Select **Accounts payable** \> **Inquiries and reports** \> **Facture**.</span></span>
6. <span data-ttu-id="556ad-221">Выберите **Печать** \> **Исходный** для счет-фактуры, созданной для налоговой проводки **Налоговый агент - начислено**.</span><span class="sxs-lookup"><span data-stu-id="556ad-221">Select **Print** \> **Original** for the facture that is created on the **Tax agent - charged** sales tax transaction.</span></span>

<span data-ttu-id="556ad-222">В отчете о счете-фактуре отображается номер и дата платежного поручения, базовая сумма без НДС и расчетная ставка налога (значение НДС ÷ значение НДС + 100).</span><span class="sxs-lookup"><span data-stu-id="556ad-222">The facture report shows the number and date of the payment order, the base amount without VAT, and the computational tax rate (VAT value ÷ VAT value + 100).</span></span>

