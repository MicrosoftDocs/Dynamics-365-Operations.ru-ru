---
title: Регистрация проводок со ссылками на договоры
description: В этой разделе представлены сведения о регистрации проводок договоров.
author: v-nadyuz
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dea995536c3aa2832d1bfa906864c99406bbc4c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997495"
---
# <a name="register-transactions-with-reference-to-agreements"></a><span data-ttu-id="597dc-103">Регистрация проводок со ссылками на договоры</span><span class="sxs-lookup"><span data-stu-id="597dc-103">Register transactions with reference to agreements</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="597dc-104">При регистрации продаж, покупок или входящих или исходящих платежей можно выполнять следующие операции:</span><span class="sxs-lookup"><span data-stu-id="597dc-104">When you register sales, purchases, or incoming or outgoing payments, you can perform the following operations:</span></span>

- <span data-ttu-id="597dc-105">Укажите ссылку на договор, в соответствии с которым выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="597dc-105">Specify a reference to the agreement that the operation is performed according to.</span></span>
- <span data-ttu-id="597dc-106">Сопоставьте проводки клиента и поставщика в контексте договоров, которые указаны во время регистрации проводок.</span><span class="sxs-lookup"><span data-stu-id="597dc-106">Settle customer and vendor transactions in the context of agreements that are specified during the registration of transactions.</span></span>

<span data-ttu-id="597dc-107">После завершения этих операций можно проанализировать оборот и сальдо по договору.</span><span class="sxs-lookup"><span data-stu-id="597dc-107">After these operations are completed, you can analyze the turnover and balance of the agreement.</span></span>

## <a name="registering-a-payment-from-a-customer-or-a-payment-to-a-vendor-and-including-an-indication-of-the-agreement"></a><span data-ttu-id="597dc-108">Регистрация платежа от клиента или платежа поставщику и включение указания договора</span><span class="sxs-lookup"><span data-stu-id="597dc-108">Registering a payment from a customer or a payment to a vendor, and including an indication of the agreement</span></span>

<span data-ttu-id="597dc-109">В русской локализации страницы **Общий журнал**, **Журнал кассовых ордеров**, **Журнал платежей поставщикам** и **Журнал платежей клиентов** содержат раздел с информацией о договоре.</span><span class="sxs-lookup"><span data-stu-id="597dc-109">In the Russian localization, the **General journal**, **Slip journal**, **Vendor payment journal**, and **Customer payment journal** pages include a section that has information about the agreement.</span></span> <span data-ttu-id="597dc-110">Используя перечисленные журналы, можно зарегистрировать платеж от клиента или платеж поставщику и включить ссылку на договор, в соответствии с которым была выполнена проводка.</span><span class="sxs-lookup"><span data-stu-id="597dc-110">By using the journals that are listed, you can register a payment from a customer or a payment to a vendor, and include a reference to the agreement that the transaction is made according to.</span></span>

<span data-ttu-id="597dc-111">В качестве примера приведенной ниже процедуры показано, как зарегистрировать платеж поставщику в журнале платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="597dc-111">As an example, the following procedure shows how to register a payment to a vendor through the vendor payment journal.</span></span> <span data-ttu-id="597dc-112">Однако ссылка на соглашение аналогична всем остальным журналам.</span><span class="sxs-lookup"><span data-stu-id="597dc-112">However, the reference to the agreement is similar for all the other journals.</span></span>

### <a name="register-a-payment-by-using-the-vendor-payment-journal"></a><span data-ttu-id="597dc-113">Регистрация платежа с помощью журнала платежей поставщику</span><span class="sxs-lookup"><span data-stu-id="597dc-113">Register a payment by using the vendor payment journal</span></span>

1. <span data-ttu-id="597dc-114">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="597dc-114">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="597dc-115">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="597dc-115">On the Action Pane, select **Lines**.</span></span>
3. <span data-ttu-id="597dc-116">На вкладке **общие** в разделе **счет** в поле **Код соглашения** выберите номер договора, для которого была зарегистрирована проводка.</span><span class="sxs-lookup"><span data-stu-id="597dc-116">On the **General** tab, in the **Account** section, in the **Agreement ID** field, select the number of the agreement that the transaction is registered for.</span></span>

<span data-ttu-id="597dc-117">В поле **Заголовок документа** автоматически задается заголовок договора.</span><span class="sxs-lookup"><span data-stu-id="597dc-117">The **Document title** field is automatically set to the title of the agreement.</span></span>

![Страница платежей поставщикам](media/10_Vendor_payments.png)

<span data-ttu-id="597dc-119">У проводки для контрагента будет ссылка на номер договора.</span><span class="sxs-lookup"><span data-stu-id="597dc-119">The transaction for the counterparty will have a link to the agreement number.</span></span>

<span data-ttu-id="597dc-120">Для просмотра проводок для контрагента выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="597dc-120">To view transactions for a counterparty, follow one of these steps.</span></span>

   - <span data-ttu-id="597dc-121">На странице **Все поставщики** в области действий на вкладке **Поставщик** в разделе **Проводки** выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="597dc-121">On the **All vendors** page, on the Action Pane, on the **Vendor** tab, in the **Transactions** section, select **Transactions**.</span></span> <span data-ttu-id="597dc-122">На вкладке **Финансовые аналитики** в поле **Договор** отображаются сведения о договоре, для которого зарегистрирована проводка.</span><span class="sxs-lookup"><span data-stu-id="597dc-122">On the **Financial dimensions** tab, the **Agreement** field shows information about the agreement that the transaction is registered for.</span></span>
   -  <span data-ttu-id="597dc-123">На странице **Все клиенты** в области действий на вкладке **Клиент** в разделе **Проводки** выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="597dc-123">On the **All customers** page, on the Action Pane, on the **Customer** tab, in the **Transactions** section, select **Transactions**.</span></span> <span data-ttu-id="597dc-124">Затем в верхней области в разделе **Параметры страницы** выберите **Изменить режим просмотра \> Представление сведений**.</span><span class="sxs-lookup"><span data-stu-id="597dc-124">Then, in the upper pane, in the **Page options** section, select **Change view \> Details view**.</span></span> <span data-ttu-id="597dc-125">На экспресс-вкладке **Финансовые аналитики** в поле **Договор** отображаются сведения о договоре, для которого зарегистрирована проводка.</span><span class="sxs-lookup"><span data-stu-id="597dc-125">On the **Financial dimensions** FastTab, the **Agreement** field shows information about the agreement that the transaction is registered for.</span></span>

## <a name="registering-accounts-receivable-or-accounts-payable-and-including-an-indication-of-the-agreement"></a><span data-ttu-id="597dc-126">Регистрация расчетов с клиентами или расчетов с поставщиками, включая указание договора</span><span class="sxs-lookup"><span data-stu-id="597dc-126">Registering accounts receivable or accounts payable, and including an indication of the agreement</span></span>

<span data-ttu-id="597dc-127">Можно регистрировать расчеты с клиентами или расчеты с поставщиками, а также включать ссылку на договор в заказ на продажу или в заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="597dc-127">You can register accounts receivable or accounts payable, and include a reference to the agreement in the sales order or the purchase order.</span></span> <span data-ttu-id="597dc-128">Дополнительные сведения см. в разделе [Выполнение договоров продажи](../../supply-chain/sales-marketing/tasks/fulfill-sales-agreements.md) и [создание заказа на запуск в производство на основе договора покупки](../../supply-chain/procurement/tasks/create-purchase-release-order-purchase-agreement.md).</span><span class="sxs-lookup"><span data-stu-id="597dc-128">For more information, see [Fulfill sales agreements](../../supply-chain/sales-marketing/tasks/fulfill-sales-agreements.md) and [Create a purchase release order from a purchase agreement](../../supply-chain/procurement/tasks/create-purchase-release-order-purchase-agreement.md).</span></span>

<span data-ttu-id="597dc-129">Можно также зарегистрировать расчеты с клиентами или расчеты с поставщиками на страницах **Накладная с произвольным текстом** и **Общие журналы**.</span><span class="sxs-lookup"><span data-stu-id="597dc-129">You can also register accounts receivable or accounts payable on the **Free text invoice** and **General journals** pages.</span></span> <span data-ttu-id="597dc-130">В русской локализации можно указать договор клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="597dc-130">In the Russian localization, you can specify a customer or vendor agreement.</span></span>

### <a name="register-accounts-receivable-by-using-a-free-text-invoice"></a><span data-ttu-id="597dc-131">Регистрация расчетов с поставщиками по накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="597dc-131">Register accounts receivable by using a free text invoice</span></span>

1. <span data-ttu-id="597dc-132">На странице **Накладная с произвольным текстом** создайте накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="597dc-132">On the **Free text invoice** page, create a free text invoice.</span></span>
2. <span data-ttu-id="597dc-133">На экспресс- вкладке **Заголовок накладной с произвольным текстом** в разделе **Договор** в поле **Код договора** выберите номер договора.</span><span class="sxs-lookup"><span data-stu-id="597dc-133">On the **Free text invoice header** FastTab, in the **Agreement** section, in the **Agreement ID** field, select the number of the agreement.</span></span>

    <span data-ttu-id="597dc-134">В поле **Заголовок документа** автоматически задается заголовок договора.</span><span class="sxs-lookup"><span data-stu-id="597dc-134">The **Document title** field is automatically set to the title of the agreement.</span></span>

    ![Страница накладной с произвольным текстом](media/11_Free_text_invoice.png)

3. <span data-ttu-id="597dc-136">Укажите другие сведения и разнесите накладную.</span><span class="sxs-lookup"><span data-stu-id="597dc-136">Specify other details, and post the invoice.</span></span>

### <a name="register-accounts-receivable-and-accounts-payable-from-general-journals"></a><span data-ttu-id="597dc-137">Регистрация расчетов с клиентами и расчетов с поставщиками из общих журналов</span><span class="sxs-lookup"><span data-stu-id="597dc-137">Register accounts receivable and accounts payable from general journals</span></span>

1. <span data-ttu-id="597dc-138">Перейдите в раздел **Главная книга** \> **Записи в журнале** \> **Общие журналы**.</span><span class="sxs-lookup"><span data-stu-id="597dc-138">Go to **General ledger** \> **Journal entries** \> **General journals**.</span></span>
2. <span data-ttu-id="597dc-139">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="597dc-139">On the Action Pane, select **Lines**.</span></span>
3. <span data-ttu-id="597dc-140">Создайте строку, затем на вкладке **Общие** в разделе **Договоры** в поле **Код соглашения** выберите номер договора, для которого была зарегистрирована проводка.</span><span class="sxs-lookup"><span data-stu-id="597dc-140">Create a line, and then, on the **General** tab, in the **Agreements** section, in the **Agreement ID** field, select the number of the agreement that the transaction is registered for.</span></span>

    <span data-ttu-id="597dc-141">В поле **Заголовок документа** автоматически задается заголовок договора.</span><span class="sxs-lookup"><span data-stu-id="597dc-141">The **Document title** field is automatically set to the title of the agreement.</span></span>

    ![Страница Ваучера журнала](media/12_Journal_voucher.png)

4. <span data-ttu-id="597dc-143">Укажите другие сведения, а затем на панели операций выберите **Разнести**, чтобы разнести проводку.</span><span class="sxs-lookup"><span data-stu-id="597dc-143">Specify other details, and then, on the Action Pane, select **Post** to post the transaction.</span></span>

## <a name="settling-factures-on-a-counterparty-in-the-context-of-agreements"></a><span data-ttu-id="597dc-144">Сопоставьте фактуры для контрагента в контексте договоров</span><span class="sxs-lookup"><span data-stu-id="597dc-144">Settling factures on a counterparty in the context of agreements</span></span>

<span data-ttu-id="597dc-145">Дополнительные сведения об управлении аналитиками для сопоставлений см. в разделе [Настройка контроля аналитик для сопоставлений (Россия)](rus-transactions-settlement-date.md).</span><span class="sxs-lookup"><span data-stu-id="597dc-145">For more information about dimension control for settlements, see [Set up dimension control for settlements (Russia)](rus-transactions-settlement-date.md).</span></span>

### <a name="settle-factures-on-a-customer-in-the-context-of-agreements"></a><a name="settle-factures-customer-agreements"></a><span data-ttu-id="597dc-146">Сопоставьте фактуры для клиента в контексте договоров</span><span class="sxs-lookup"><span data-stu-id="597dc-146">Settle factures on a customer in the context of agreements</span></span>

1. <span data-ttu-id="597dc-147">Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="597dc-147">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
2. <span data-ttu-id="597dc-148">На вкладке **Сбор** в разделе **Сопоставление** выберите **Сопоставление фактур с оплатами**.</span><span class="sxs-lookup"><span data-stu-id="597dc-148">On the **Collect** tab, in the **Settle** section, select **Facture and payment settlement**.</span></span>

    ![Страница сопоставлений фактур с оплатами](media/13_Facture_and_payment_settlement.png)

3. <span data-ttu-id="597dc-150">В верхней и нижней областях установите следующие параметры, чтобы выбрать проводки:</span><span class="sxs-lookup"><span data-stu-id="597dc-150">In the upper and lower panes, set the following options to select transactions:</span></span>

   - <span data-ttu-id="597dc-151">В поле **Искать в** выберите **Договор**.</span><span class="sxs-lookup"><span data-stu-id="597dc-151">In the **Look in** field, select **Agreement**.</span></span>
    - <span data-ttu-id="597dc-152">В поле **Код договора** выберите договор, для которого необходимо сопоставить проводки.</span><span class="sxs-lookup"><span data-stu-id="597dc-152">In the **Agreement ID** field, select an agreement that you want to settle transactions for.</span></span>
    
    <span data-ttu-id="597dc-153">Показаны выбранные проводки, включающие выбранный договор.</span><span class="sxs-lookup"><span data-stu-id="597dc-153">The transactions that include the selected agreement are shown.</span></span>

4. <span data-ttu-id="597dc-154">Используйте флажки **Пометка**, чтобы выбрать проводку возмещения для сопоставления в верхней области и проводку выплаты в нижней области.</span><span class="sxs-lookup"><span data-stu-id="597dc-154">Use the **Mark** check boxes to select the reimbursement transaction for settlement in the upper pane and the disbursement transaction in the lower pane.</span></span>
5. <span data-ttu-id="597dc-155">В области действий выберите **Обновить** для сопоставления проводки по контрагенту.</span><span class="sxs-lookup"><span data-stu-id="597dc-155">On the Action Pane, select **Update** to settle the counteragent transaction.</span></span>

### <a name="settle-factures-on-a-vendor-in-the-context-of-agreements"></a><span data-ttu-id="597dc-156">Сопоставьте фактуры для поставщика в контексте договоров</span><span class="sxs-lookup"><span data-stu-id="597dc-156">Settle factures on a vendor in the context of agreements</span></span>

1. <span data-ttu-id="597dc-157">Перейдите в раздел **Расчеты с поставщиками \> Поставщики \> Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="597dc-157">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
2. <span data-ttu-id="597dc-158">На вкладке **Накладная** в разделе **Сопоставление** выберите **Сопоставление фактур с оплатами**.</span><span class="sxs-lookup"><span data-stu-id="597dc-158">On the **Invoice** tab, in the **Settle** section, select **Facture and payment settlement**.</span></span>
3. <span data-ttu-id="597dc-159">Сопоставление проводок в контексте договоров, как описано в предыдущем разделе данной темы, [Сопоставьте фактуры для клиента в контексте договоров](#settle-factures-customer-agreements).</span><span class="sxs-lookup"><span data-stu-id="597dc-159">Settle transactions in the context of agreements as described in the previous section of this topic, [Settle factures on a customer in the context of agreements](#settle-factures-customer-agreements).</span></span>

### <a name="periodically-settle-sales-or-purchase-transactions"></a><span data-ttu-id="597dc-160">Периодическое сопоставление проводок по продажам или покупкам</span><span class="sxs-lookup"><span data-stu-id="597dc-160">Periodically settle sales or purchase transactions</span></span>

<span data-ttu-id="597dc-161">Можно выполнить периодическое сопоставление проводок по контрагентам, используя страницу **Периодическое сопоставление**, если для параметра **Разрешить автоматическое сопоставление** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="597dc-161">You can do periodic settlement of counteragent transactions by using the **Periodic settlement** page if the **Allow automatic settlement** option is set to **Yes**.</span></span> <span data-ttu-id="597dc-162">Можно сторнировать сопоставление на странице **Периодический реверс**.</span><span class="sxs-lookup"><span data-stu-id="597dc-162">You can reverse the settlement on the **Periodic reverse** page.</span></span>

<span data-ttu-id="597dc-163">В качестве примера можно выполнить периодическое сопоставление проводок по продажам.</span><span class="sxs-lookup"><span data-stu-id="597dc-163">As an example, this procedure shows how to do periodic settlement of sales transactions.</span></span>

1. <span data-ttu-id="597dc-164">Выберите **Расчеты с клиентами** \> **Настройка** \> **Профили разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="597dc-164">Go to **Accounts receivable** \> **Setup** \> **Customer posting profiles**.</span></span>
2. <span data-ttu-id="597dc-165">Выберите профиль разноски клиента, а затем на экспресс-вкладке **Табличные ограничения** установите для параметра **Разрешить автоматическое сопоставление** значение **Да**, чтобы разрешить автоматическое сопоставление проводок по продажам.</span><span class="sxs-lookup"><span data-stu-id="597dc-165">Select a customer posting profile, and then, on the **Table restrictions** FastTab, set the **Allow automatic settlement** option to **Yes** to allow for automatic settlement of sales transactions.</span></span>
3. <span data-ttu-id="597dc-166">Перейдите **Расчеты с клиентами** \> **Периодические задачи** \> **Сопоставление** \> **Периодические сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="597dc-166">Go to **Accounts receivable** \> **Periodic tasks** \> **Settlement** \> **Periodic settlements**.</span></span>
4. <span data-ttu-id="597dc-167">На странице **Периодические сопоставления** укажите сведения, а затем нажмите **OK**, чтобы выполнить сопоставление.</span><span class="sxs-lookup"><span data-stu-id="597dc-167">On the **Periodic settlements** page, specify the details, and then select **OK** to do the settlement.</span></span>

<span data-ttu-id="597dc-168">Для сторнирования сопоставления **Расчеты с клиентами** \> **Периодические задачи** \> **Сопоставление** \> **Периодический реверс**.</span><span class="sxs-lookup"><span data-stu-id="597dc-168">To reverse the settlement, go to **Accounts receivable** \> **Periodic tasks** \> **Settlement** \> **Periodic reverse**.</span></span> <span data-ttu-id="597dc-169">На странице **Периодический реверс** укажите сведения, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="597dc-169">On the **Periodic reverse** page, specify the details, and then select **OK**.</span></span>

<span data-ttu-id="597dc-170">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="597dc-170">Find more details in the following topics:</span></span>

- [<span data-ttu-id="597dc-171">Договоры</span><span class="sxs-lookup"><span data-stu-id="597dc-171">Agreements</span></span>](rus-agreements.md)
- [<span data-ttu-id="597dc-172">Настройка и создание договоров</span><span class="sxs-lookup"><span data-stu-id="597dc-172">Set up and create agreements</span></span>](rus-set-up-and-create-agreements.md)
- [<span data-ttu-id="597dc-173">Запросы и отчеты с договорами</span><span class="sxs-lookup"><span data-stu-id="597dc-173">Inquiries and reports with agreements</span></span>](rus-inquiries-reports-agreements.md)
